#Complete Example DZIF 2016
=================================
This documentation page aims to be a complete example walk through for the usage of the CONCOCT package version 
0.4 except for the assembly and COG annotations step.

It is not required to run all steps. The output files for each step are in the test data repository. 
At the end of this example the results should be the same as the results in the corresponding 
test data repository. The version numbers listed above are the ones used to generate the results in that repository. 
Using newer versions will probably not be a problem, but your results may be different in that case.

##Login to your VM
-----------------------

You need to create a VM from the image CONCOCT-Tutorial login to it (**ssh -Y**) and then set the permissions on the ephemeral disk:

```
sudo umount /mnt 
sudo mkfs.xfs -f /dev/vdb
sudo mount /dev/vdb /mnt/
sudo chown ubuntu:ubuntu /mnt
```

##Setting up the test environment
-------------------------------
Move to your mnt directory, create a folder where you want all the output from this example to go:

```
    cd /mnt
    mkdir CONCOCT-complete-example
    cd CONCOCT-complete-example
```

Set two variables with full paths. One pointing to the root directory of the ```CONCOCT``` software, one pointing to the test data repository, named ```CONCOCT_TEST``` and one to the directory we just created. 

```
    export CONCOCT=/home/ubuntu/Installed/CONCOCT
    export CONCOCT_EXAMPLE=/mnt/CONCOCT-complete-example
```

You can see the full path of a directory you are located in by running the command ```pwd```.

Copy in the example data from the class folder:
```
    cp ~/Data/Example.tar.gz .
```

And extract:
```
    tar -xvzf Example.tar.gz
```

##Assembling Metagenomic Reads
----------------------------
The first step in the analysis is to assemble all reads into contigs, even 
for this small example, 1 million reads per sample and 16 samples, this is computationally 
intensive. There are a number of assemblers available if you want a quick results megahit 
generally performs well but Spades is also good. The best choice is data set dependent.

Then assemble the reads. We recommend megahit for this. To perform the assembly I ran the 
following commands, please **do not run this**:

```
cd Example 
megahit -1 $(<R1.csv) -2 $(<R2.csv) -t 8 -o Assembly --presets meta 
mv Assembly ..
cd ..
```

However, I **do not** suggest you do this now instead copy the contigs from the Data folder:

```
    mkdir Assembly
    cp ~/Data/final.contigs.fa Assembly
```


##Cutting up contigs
----------------------------
In order to give more weight to larger contigs and mitigate the effect of assembly errors 
we cut up the contigs into chunks of 10 Kb. The final chunk is appended to the one before 
it if it is < 10 Kb to prevent generating small contigs. This means that no contig < 20 Kb is cut up. 
We use the script ``cut_up_fasta.py`` for this:

Now lets cut up the contigs and index for the mapping program bwa:
```
mkdir contigs
python $CONCOCT/scripts/cut_up_fasta.py -c 10000 -o 0 -m Assembly/final.contigs.fa > contigs/final_contigs_c10K.fa
```


##Map the Reads onto the Contigs
------------------------------
After assembly we map the reads of each sample back to the assembly using [bwa](https://github.com/lh3/bwa).


```
cd contigs
bwa index final_contigs_c10K.fa
$CONCOCT/scripts/Lengths.pl final_contigs_c10K.fa > final_contigs_c10K.len
cd ..

mkdir Map

for file in Example/*R1.fastq
do 
   
   stub=${file%_R1.fastq}
   stub2=${stub#Example\/}	
   echo $stub

   file2=${stub}_R2.fastq

   bwa mem -t 8 contigs/final_contigs_c10K.fa $file $file2 > Map/${stub2}.sam
done
```

Followed by these:

```
for file in Map/*.sam
do
    stub=${file%.sam}
    stub2=${stub#Map\/}
    echo $stub	
    samtools view -h -b -S $file > ${stub}.bam
    samtools view -b -F 4 ${stub}.bam > ${stub}.mapped.bam
    samtools sort -m 1000000000 ${stub}.mapped.bam ${stub}.mapped.sorted
    bedtools genomecov -ibam ${stub}.mapped.sorted.bam -g contigs/final_contigs_c10K.len > ${stub}_cov.txt
done
```

and:

```
for i in Map/*_cov.txt 
do 
   echo $i
   stub=${i%_cov.txt}
   stub=${stub#Map\/}
   echo $stub
   awk -F"\t" '{l[$1]=l[$1]+($2 *$3);r[$1]=$4} END {for (i in l){print i","(l[i]/r[i])}}' $i > Map/${stub}_cov.csv
done
```

This is quite complex and slow. If you like just copy the precomputed files instead:

```
    cp ~/Data/Map.tar.gz $CONCOCT_EXAMPLE
    cd $CONCOCT_EXAMPLE
    tar -xvzf Map.tar.gz
```

##Generate coverage table
------------------------

Given the processed mapping files we can now generate the coverage table:

```
$CONCOCT/scripts/Collate.pl $CONCOCT_EXAMPLE/Map | tr "," "\t" > Coverage.tsv
```

This is a simple tab delimited file with the coverage of each contig per sample.


##Run concoct
-----------

To see possible parameter settings with a description run

```
    concoct --help
```

We will only run concoct for some standard settings here. The only one we vary is the cluster number which should be at least twice the number of genomes in your 
co-assembly (see discussion below of how to estimate this). In this case we know it is 
around 20 so run concoct with 40 as the maximum number of cluster `-c 40`:

```
mkdir Concoct
cd Concoct
mv ../Coverage.tsv .
concoct --coverage_file Coverage.tsv --composition_file ../contigs/final_contigs_c10K.fa -c 40
cd ..
```

When concoct has finished the message "CONCOCT Finished, the log shows how it went." is piped to stdout. The program generates a number of files in the output directory that can be set with the `-b` parameter and will be the present working directory by default. 

##Contig annotation

We are going to annotate COGs on our contigs. You first need to find genes on the contigs and 
functionally annotate these. Here we used prodigal (https://github.com/hyattpd/Prodigal) for 
gene prediction and annotation, but you can use anything you want:

```
mkdir Annotate_gt1000
cd Annotate_gt1000
$CONCOCT/scripts/LengthFilter.pl ../contigs/final_contigs_c10K.fa 1000 > final_contigs_gt1000_c10K.fa
prodigal -i final_contigs_gt1000_c10K.fa -a final_contigs_gt1000_c10K.faa -d final_contigs_gt1000_c10K.fna  -f gff -p meta -o final_contigs_gt1000_c10K.gff
```

Then we assigned COGs (but on another server) - **do not run this**

```
export COGSDB_DIR=/home/opt/rpsblast_db
nohup $CONCOCT/scripts/RPSBLAST.sh -f final_contigs_gt1000_c10K.faa -p -c 32 -r 1 > r.out&
```

Instead just copy the blast results into your Annotate_gt1000 directory:

```
cd $CONCOCT_EXAMPLE/Annotate_gt1000
cp ~/Data/final_contigs_gt1000_c10K.out .
cd ..
```

How to determine number of genomes present?

```
cd Annotate_gt1000
python $CONCOCT/scripts/ExtractCogs.py -b final_contigs_gt1000_c10K.out --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv > final_contigs_gt1000_c10K.cogs
$CONCOCT/scripts/CountSCGs.pl $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_generaR.txt < final_contigs_gt1000_c10K.cogs  | cut -d"," -f2 | awk -f $CONCOCT/scripts/median.awk
```

The result should be 12.5, this places an upper limit on the number of genomes we can bin.

##Evaluate output
---------------

This will require that you have Rscript with the R packages [gplots](http://cran.r-project.org/web/packages/gplots/index.html), [reshape](http://cran.r-project.org/web/packages/reshape/index.html), [ggplot2](http://cran.r-project.org/web/packages/ggplot2/index.html), [ellipse](http://cran.r-project.org/web/packages/ellipse/index.html), [getopt](http://cran.r-project.org/web/packages/getopt/index.html) and [grid](http://cran.r-project.org/web/packages/grid/index.html) installed. The package grid does not have to be installed for R version > 1.8.0

First we can visualise the clusters in the first two PCA dimensions:

```
cd $CONCOCT_EXAMPLE
mkdir evaluation-output
Rscript $CONCOCT/scripts/ClusterPlot.R -c Concoct/clustering_gt1000.csv -p Concoct/PCA_transformed_data_gt1000.csv -m Concoct/pca_means_gt1000.csv -r Concoct/pca_variances_gt1000_dim -l -o evaluation-output/ClusterPlot.pdf
```


To visualise your plots if you have x-windows forwarding just try:
```
evince evaluation-output/ClusterPlot.pdf
```

If that fails you will have to copy them off the server to a local directory. 

The figure should look like this:

![Cluster PCA](figsD/ClusterPlot.pdf)


We can also compare the clustering to species labels. For this test data set we know these labels, they are given in the file ```$CONCOCT_TEST/AssignGenome/clustering_gt1000_smap.csv```. For real data labels may be obtained through taxonomic classification.
In either case we provide a script Validate.pl for computing basic metrics on the cluster quality. Lets copy the validation data into our directory:

```
cd $CONCOCT_EXAMPLE
mkdir AssignGenome
cp ~/Data/clustering_gt1000_smap.csv AssignGenome
```

And run our validation script:
```
cd evaluation-output
$CONCOCT/scripts/Validate.pl --cfile=../Concoct/clustering_gt1000.csv --sfile=../AssignGenome/clustering_gt1000_smap.csv --ffile=../Annotate_gt1000/final_contigs_gt1000_c10K.fa --ofile=clustering_gt1000_conf.csv
```

 This script requires the clustering output by concoct ```Concoct/clustering_gt1000.csv``` these have a simple format of a comma separated file listing each contig id followed by the cluster index and the species labels that have the same format but with a text label rather than a cluster index. The script should output:

```
N	M	TL	S	K	Rec.	Prec.	NMI	Rand	AdjRand
11519	11519	5.3364e+07	20	25	0.994171	0.990678	0.990872	0.998723	0.989500
```

This gives the no. of contigs N clustered, the number with labels M, the number of unique labels S, 
the number of clusters K, the recall, the precision, the normalised mutual information (NMI), the Rand index, and the adjusted Rand index. It also generates a file called a `confusion matrix` with the frequencies of each species in each cluster. We provide a further script for visualising this as a heatmap:

```
cd $CONCOCT_EXAMPLE
Rscript $CONCOCT/scripts/ConfPlot.R  -c evaluation-output/clustering_gt1000_conf.csv -o  evaluation-output/clustering_gt1000_conf.pdf
```

This generates a file with normalised frequencies of contigs from each cluster across species:

![Confusion matrix](figsD/clustering_gt1000_conf.pdf)


To view this you can download off server of use evince if you loggin in with -y:

```
evince evaluation-output/clustering_gt1000_conf.pdf .
```

##Validation using single-copy core genes
---------------------------------------

We can also evaluate the clustering based on single-copy core genes. We will use our results from above in ```Annotate_gt1000``` to do this.

```
cd $CONCOCT_EXAMPLE 
$CONCOCT/scripts/COG_table.py -b Annotate_gt1000/final_contigs_gt1000_c10K.out -m $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_genera.txt -c  Concoct/clustering_gt1000.csv --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv > evaluation-output/clustering_gt1000_scg.tab
```

The script requires the clustering output by concoct ```concoct-output/clustering_gt1000.csv```, a file listing a set of SCGs (e.g. a set of COG ids) to use ```scgs/scg_cogs_min0.97_max1.03_unique_genera.txt``` and a mapping of Conserved Domain Database ids (https://www.ncbi.nlm.nih.gov/Structure/cdd/cdd.shtml) to COG ids ``$CONCOCT/scgs/cdd_to_cog.tsv``.

The output file is a tab-separated file with basic information about the clusters (cluster id, ids of contigs in cluster and number of contigs in cluster) in the first three columns, and counts of the different SCGs in the following columns.

This can also be visualised graphically using the R script:

```
cd $CONCOCT_EXAMPLE
Rscript $CONCOCT/scripts/COGPlot.R -s evaluation-output/clustering_gt1000_scg.tab -o evaluation-output/clustering_gt1000_scg.pdf
```

To view this use evince again:

```
evince evaluation-output/clustering_gt1000_scg.pdf 
```

The plot is downloadable here:

![scg plot](figsD/clustering_gt1000_scg.pdf)

How many 75% complete genomes did we get. Do this yourselves in R.
```
R
> scg <- read.table("evaluation-output/clustering_gt1000_scg.tab",header=TRUE,row.names=1)
> scg <- scg[,-1]
> scg <- scg[,-1]
>sum(rowSums(scg == 1)/36. > 0.75)
>q()
```

We got 12 75% complete genomes.

##Comparison to MetaBat

We will also compare to a competitor algorithm released last year [MetaBat](https://bitbucket.org/berkeleylab/metabat) and 
[paper](https://peerj.com/articles/1165/). Note the claim 
"MetaBAT outperforms alternative methods in accuracy and computational efficiency on both synthetic and real metagenome datasets.".

```
mkdir Metabat
cd Metabat
runMetaBat.sh -m 1500 ../contigs/final_contigs_c10K.fa ../Map/Sample*_sub.bam
```

We run it on the same contigs utilising the same bam files. The minimum length that MetaBat will allow is 1500bp. So once this is done to provide a fair comparison we will 
also rerun CONCOCT with this minimum contig length.

```
cd $CONCOCT_EXAMPLE
mkdir Concoct_gt1500
cd Concoct_gt1500
concoct --coverage_file ../Concoct/Coverage.tsv --composition_file ../contigs/final_contigs_c10K.fa -c 40 -l 1500
```

Lets compare the Metabat results with CONCOCT. First we maninpulate the cluster assignments into our format:

```
cd $CONCOCT_EXAMPLE/Metabat
grep ">" final_contigs_c10K.fa.metabat-bins*fa | sed 's/.fa:>/,/g' | sed 's/final_contigs_c10K.fa.metabat-bins-_-m_1500\.//g' | awk -F, '{print $2,$1}' OFS=, > clustering_gt1500.csv
```

Then we run the validation script:
```
 $CONCOCT/scripts/Validate.pl --cfile=clustering_gt1500.csv --sfile=../AssignGenome/clustering_gt1000_smap.csv --ffile=../Annotate_gt1000/final_contigs_gt1000_c10K.fa --ofile=clustering_gt1500_conf.csv
```

```
N	M	TL	S	K	Rec.	Prec.	NMI	Rand	AdjRand
8322	8317	4.7857e+07	19	26	0.876835	0.996679	0.938554	0.983830	0.868697
```
    
We can also generate confusion plots and the the SCG table..

```
$CONCOCT/scripts/COG_table.py -b ../Annotate_gt1000/final_contigs_gt1000_c10K.out -m $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_genera.txt -c clustering_gt1500.csv --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv > clustering_gt1500_scg.tab

Rscript $CONCOCT/scripts/COGPlot.R -s clustering_gt1500_scg.tab -o metabat_clustering_gt1500_scg.pdf

Rscript $CONCOCT/scripts/ConfPlot.R  -c clustering_gt1500_conf.csv -o metabat_clustering_gt1500_conf.pdf
```

To generate:

![Metabat scg plot](figsD/metabat_clustering_gt1500_scg.pdf)

![Metabat conf plot](figsD/metabat_clustering_gt1500_conf.pdf)

These confirm that Metabat suffers from fragmentation errors. In fact we get 10 75% complete genomes.

We can compare to CONCOCT at the same contig cut-off:

```
cd $CONCOCT_EXAMPLE
cd Concoct_gt1500
$CONCOCT/scripts/Validate.pl --cfile=clustering_gt1500.csv --sfile=../AssignGenome/clustering_gt1000_smap.csv --ffile=../Annotate_gt1000/final_contigs_gt1000_c10K.fa --ofile=clustering_gt1500_conf.csv
```

```
N	M	TL	S	K	Rec.	Prec.	NMI	Rand	AdjRand
8535	8535	4.9711e+07	20	23	0.993698	0.952719	0.981084	0.994119	0.954376
```
    
Substantially better. Looking at SCGs...

```
$CONCOCT/scripts/COG_table.py -b ../Annotate_gt1000/final_contigs_gt1000_c10K.out -m $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_genera.txt -c clustering_gt1500.csv --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv > clustering_gt1500_scg.tab
Rscript $CONCOCT/scripts/COGPlot.R -s clustering_gt1500_scg.tab -o concoct_clustering_gt1500_scg.pdf
Rscript $CONCOCT/scripts/ConfPlot.R  -c clustering_gt1500_conf.csv -o concoct_clustering_gt1500_conf.pdf
```

Now we have 10. So the same as metabat :( CONCOCT as overclustered two of the species.

![CONCOCT scg plot](figsD/concoct_clustering_gt1500_scg.pdf)

![CONCOCT conf plot](figsD/concoct_clustering_gt1500_conf.pdf)