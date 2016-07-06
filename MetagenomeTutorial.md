#Metagenome Tutorial (CENTA 10th June)

##Getting started

Login to your VM and as before move to the Projects directory:

```
cd Projects
```

## Taxonomic profiling

Today we are going to profile using [Metaphlan2](https://bitbucket.org/biobakery/metaphlan2) which is an easy to used read 
based metagenome profiler that uses a precomputed database of genes that are unique and characteristic of particular 
taxa. It requires the read mapper [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml) which is preinstalled on the VM. 
We are going to test it out on some fecal samples from healthy controls and children with Crohn's from the CICRA study.

Expand out the example data directory:
```
tar -xvzf MetaTutorial.tar.gz
``` 

Inside this directory are twenty fasta files. One for each sample. Have a look at one:
```
more MetaTutorial/C1_R12.fasta
```
These actually contained trimmed forward and reverse sequences collated together. More typically you might work 
with separate fastq files.

How to count the number of reads in a fasta file?
```
grep -c ">" MetaTutorial/C1_R12.fasta
```

Then run Metaphlan2 on 8 processors making a results directory for the output first:
```
mkdir MetaphlanResults
metaphlan2.py MetaTutorial/C1_R12.fasta --input_type fasta --nproc 8 > MetaphlanResults/C1_profiled_metagenome.txt
``` 

The output simply the gives the proportion of different taxa predicted at increasing levels of resolution.
```
more MetaphlanResults/C1_profiled_metagenome.txt
```

Now we are going to run all our samples in one go. This block of code must be entered together:
```
for file in MetaTutorial/*_R12.fasta
do
    stub=${file%_R12.fasta}
    stub=${stub#MetaTutorial\/}
    echo $stub
    metaphlan2.py $file --input_type fasta --nproc 8 > MetaphlanResults/${stub}_pm.txt
done
```

Then when we are done we merge these tables:
```
python ~/Installed/metaphlan2/utils/merge_metaphlan_tables.py MetaphlanResults/*_pm.txt > MetaphlanMerged/merged_abundance_table.txt
```

and generate a heatmap:
```
python ~/Installed/metaphlan2/utils/metaphlan_hclust_heatmap.py -c bbcry --top 25 --minv 0.1 -s log --in MetaphlanMerged/merged_abundance_table.txt --out MetaphlanMerged/abundance_heatmap.png
```

##Assembly based metagenomics analysis

We are now going to perform a basic assembly based metagenomics analysis of these same samples. This will involve 
a collection of different software programs:

1. [megahit](https://github.com/voutcn/megahit): A highly efficient metagenomics assembler currently our default for most studies

2. [bwa](https://github.com/lh3/bwa): Necessary for mapping reads onto contigs

3. [samtools] (http://www.htslib.org/download/): Utilities for processing mapped files

4. [CONCOCT](https://github.com/BinPro/CONCOCT): Our own contig binning algorithm

5. [prodigal] (https://github.com/hyattpd/prodigal/releases/): Used for calling genes on contigs

6. [gnu parallel] (http://www.gnu.org/software/parallel/): Used for parallelising rps-blast

7. [standalone blast] (http://www.ncbi.nlm.nih.gov/books/NBK52640/): Needs rps-blast

8. [COG RPS database] (ftp://ftp.ncbi.nih.gov/pub/mmdb/cdd/little_endian/): Cog databases

9. [GFF python parser] (https://github.com/chapmanb/bcbb/tree/master/gff)

#Co-assembly

We begin by performing a co-assembly of these samples using a program called megahit:

```
cat MetaTutorial/*R12.fasta > MetaTutorial/All_R12.fasta
megahit -r MetaTutorial/All_R12.fasta --presets meta -o Coassembly -t 8
```

We can have a look at how good the assembly was:
```
contig-stats.pl < Coassembly/final.contigs.fa
```
Not great, but expected given the low read number.

We will now perform CONCOCT binning of these contigs. As explained in [Alneberg et al.](http://www.nature.com/nmeth/journal/v11/n11/full/nmeth.3103.html) 
there are good reasons to cut up contigs prior to binning. We will use a script from CONCOCT to do this. For convenience we 
have created an environmental variables that points to the CONCOCT install directory:
```
echo $CONCOCT
```

###Mapping

First we cut up contigs and place in new dir:

```bash
mkdir contigs
python $CONCOCT/scripts/cut_up_fasta.py -c 10000 -o 0 -m Coassembly/final.contigs.fa > contigs/final_contigs_c10K.fa
```

Having cut-up the contigs the next step is to map all the reads from each sample back onto them. First index the contigs with bwa:

```bash
cd contigs
bwa index final_contigs_c10K.fa
cd ..
```

Then perform the actual mapping you may want to put this in a shell script:

```bash
mkdir Map

for file in MetaTutorial/{C,H}*R12.fasta
do 
   
   stub=${file%_R12.fasta}
   stub=${stub#MetaTutorial\/}
   echo $stub

   bwa mem -t 8 contigs/final_contigs_c10K.fa $file > Map/${stub}.sam
done
```

Here we are using 8 threads for bwa mem '-t 8' you can adjust this to whatever is suitable for your machine.
Then we need to calculate our contig lengths.

```bash
python ~/bin/Lengths.py -i contigs/final_contigs_c10K.fa > contigs/final_contigs_c10K.len
```

Then we calculate coverages for each contig in each sample:

```bash
for file in Map/*.sam
do
    stub=${file%.sam}
    stub2=${stub#Map\/}
    echo $stub	
    samtools view -h -b -S $file > ${stub}.bam 
    samtools view -b -F 4 ${stub}.bam > ${stub}.mapped.bam
    samtools sort ${stub}.mapped.bam ${stub}.mapped.sorted
    bedtools genomecov -ibam ${stub}.mapped.sorted.bam -g contigs/final_contigs_c10K.len > ${stub}_cov.txt
done
```

and use awk to aggregate the output of bedtools:

```bash
for i in Map/*_cov.txt 
do 
   echo $i
   stub=${i%_cov.txt}
   stub=${stub#Map\/}
   echo $stub
   awk -F"\t" '{l[$1]=l[$1]+($2 *$3);r[$1]=$4} END {for (i in l){print i","(l[i]/r[i])}}' $i > Map/${stub}_cov.csv
done
```

and finally run the following perl script to collate the coverages across samples, where we have simply adjusted the format 
from csv to tsv to be compatible with CONCOCT:

```bash
Collate.pl Map | tr "," "\t" > Coverage.tsv
```

###Run CONCOCT

and run CONCOCT:
```bash
mkdir Concoct
cd Concoct
mv ../Coverage.tsv .
concoct --coverage_file Coverage.tsv --composition_file ../contigs/final_contigs_c10K.fa -c 40
cd ..
```

###Gene annotation on contigs

Run prodigal to annotate genes:
```
mkdir Annotate
cd Annotate/
LengthFilter.pl ../contigs/final_contigs_c10K.fa 1000 > final_contigs_gt1000_c10K.fa
prodigal -i final_contigs_gt1000_c10K.fa -a final_contigs_gt1000_c10K.faa -d final_contigs_gt1000_c10K.fna  -f gff -p meta -o final_contigs_gt1000_c10K.gff
```

And annotate to COGs:
```
rpsblast -i final_contigs_gt1000_c10K.faa -d ~/Databases/rpsblast_db/Cog -e 0.00001 -m 8  >  final_contigs_gt1000_c10K.rpsblast
```

Then generate SCG frequencies in clusters:
```
$CONCOCT/scripts/COG_table.py -b final_contigs_gt1000_c10K.rpsblast -m $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_genera.txt -c ../Concoct/clustering_gt1000.csv --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv > clustering_gt1000_scg.tsv
```

and a pdf:
```
$CONCOCT/scripts/COGPlot.R -s clustering_gt1000_scg.tsv -o clustering_gt1000_scg.pdf
```