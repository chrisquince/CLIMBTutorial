



<!DOCTYPE html>
<html lang="en" class="">
  <head prefix="og: http://ogp.me/ns# fb: http://ogp.me/ns/fb# object: http://ogp.me/ns/object# article: http://ogp.me/ns/article# profile: http://ogp.me/ns/profile#">
    <meta charset='utf-8'>
    

    <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/frameworks-130b94ff796a9660d814b59665547ebaf99cc439323c908f41c6ff46e4255c8e.css" media="all" rel="stylesheet" />
    <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/github-3af853ae6f7ebef8cc4949b68b4ef8e241b6561aeeb1a6b8efa2030a46e68b11.css" media="all" rel="stylesheet" />
    
    
    <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/site-becbb68a5e0ae3f94214b9e9edea2c49974f6d60b9eae715b70e5d017ff1b935.css" media="all" rel="stylesheet" />
    

    <link as="script" href="https://assets-cdn.github.com/assets/frameworks-f2534631b1ca6bf10c7effe73f9786cc1fb3426f2674a91519497864b6648282.js" rel="preload" />
    
    <link as="script" href="https://assets-cdn.github.com/assets/github-a87b249a8cd99dc3cc1181de10363bf4977348a01f2cc65cd08a0e6af5550176.js" rel="preload" />

    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta http-equiv="Content-Language" content="en">
    <meta name="viewport" content="width=device-width">
    
    <title>CONCOCT/complete_example2016.md at STAMPS · BinPro/CONCOCT · GitHub</title>
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
    <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
    <link rel="apple-touch-icon" href="/apple-touch-icon.png">
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-57x57.png">
    <link rel="apple-touch-icon" sizes="60x60" href="/apple-touch-icon-60x60.png">
    <link rel="apple-touch-icon" sizes="72x72" href="/apple-touch-icon-72x72.png">
    <link rel="apple-touch-icon" sizes="76x76" href="/apple-touch-icon-76x76.png">
    <link rel="apple-touch-icon" sizes="114x114" href="/apple-touch-icon-114x114.png">
    <link rel="apple-touch-icon" sizes="120x120" href="/apple-touch-icon-120x120.png">
    <link rel="apple-touch-icon" sizes="144x144" href="/apple-touch-icon-144x144.png">
    <link rel="apple-touch-icon" sizes="152x152" href="/apple-touch-icon-152x152.png">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180x180.png">
    <meta property="fb:app_id" content="1401488693436528">

      <meta content="https://avatars1.githubusercontent.com/u/3515015?v=3&amp;s=400" name="twitter:image:src" /><meta content="@github" name="twitter:site" /><meta content="summary" name="twitter:card" /><meta content="BinPro/CONCOCT" name="twitter:title" /><meta content="CONCOCT - Clustering cONtigs with COverage and ComposiTion" name="twitter:description" />
      <meta content="https://avatars1.githubusercontent.com/u/3515015?v=3&amp;s=400" property="og:image" /><meta content="GitHub" property="og:site_name" /><meta content="object" property="og:type" /><meta content="BinPro/CONCOCT" property="og:title" /><meta content="https://github.com/BinPro/CONCOCT" property="og:url" /><meta content="CONCOCT - Clustering cONtigs with COverage and ComposiTion" property="og:description" />
      <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">
    <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">
    <link rel="assets" href="https://assets-cdn.github.com/">
    
    <meta name="pjax-timeout" content="1000">
    
    <meta name="request-id" content="C325EA3E:66B1:114429E6:57C6A844" data-pjax-transient>

    <meta name="msapplication-TileImage" content="/windows-tile.png">
    <meta name="msapplication-TileColor" content="#ffffff">
    <meta name="selected-link" value="repo_source" data-pjax-transient>

    <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
<meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-analytics" content="UA-3769691-2">

<meta content="collector.githubapp.com" name="octolytics-host" /><meta content="github" name="octolytics-app-id" /><meta content="C325EA3E:66B1:114429E6:57C6A844" name="octolytics-dimension-request_id" />
<meta content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" name="analytics-location" />



  <meta class="js-ga-set" name="dimension1" content="Logged Out">



        <meta name="hostname" content="github.com">
    <meta name="user-login" content="">

        <meta name="expected-hostname" content="github.com">
      <meta name="js-proxy-site-detection-payload" content="NzBmZjdhOTA2NTEyZWM0Nzg0NzYxYTVjNTdkYTE0ZmE0NmFlZWIzMDJjMTJiMGJiNGVkN2Q0OTcyOTc4MzY5Znx7InJlbW90ZV9hZGRyZXNzIjoiMTk1LjM3LjIzNC42MiIsInJlcXVlc3RfaWQiOiJDMzI1RUEzRTo2NkIxOjExNDQyOUU2OjU3QzZBODQ0IiwidGltZXN0YW1wIjoxNDcyNjM2OTk2fQ==">


      <link rel="mask-icon" href="https://assets-cdn.github.com/pinned-octocat.svg" color="#4078c0">
      <link rel="icon" type="image/x-icon" href="https://assets-cdn.github.com/favicon.ico">

    <meta name="html-safe-nonce" content="2dd16b17b2b9066f7be03f51cd6b198f97a05f35">
    <meta content="2aa4571a05a5144e553661e03394814607555cee" name="form-nonce" />

    <meta http-equiv="x-pjax-version" content="5656fed6766578b36e2098085a5bb44b">
    

      
  <meta name="description" content="CONCOCT - Clustering cONtigs with COverage and ComposiTion">
  <meta name="go-import" content="github.com/BinPro/CONCOCT git https://github.com/BinPro/CONCOCT.git">

  <meta content="3515015" name="octolytics-dimension-user_id" /><meta content="BinPro" name="octolytics-dimension-user_login" /><meta content="11156601" name="octolytics-dimension-repository_id" /><meta content="BinPro/CONCOCT" name="octolytics-dimension-repository_nwo" /><meta content="true" name="octolytics-dimension-repository_public" /><meta content="false" name="octolytics-dimension-repository_is_fork" /><meta content="11156601" name="octolytics-dimension-repository_network_root_id" /><meta content="BinPro/CONCOCT" name="octolytics-dimension-repository_network_root_nwo" />
  <link href="https://github.com/BinPro/CONCOCT/commits/STAMPS.atom" rel="alternate" title="Recent Commits to CONCOCT:STAMPS" type="application/atom+xml">


      <link rel="canonical" href="https://github.com/BinPro/CONCOCT/blob/STAMPS/doc/complete_example2016.md" data-pjax-transient>
  </head>


  <body class="logged-out  env-production  vis-public page-blob">
    <div id="js-pjax-loader-bar" class="pjax-loader-bar"><div class="progress"></div></div>
    <a href="#start-of-content" tabindex="1" class="accessibility-aid js-skip-to-content">Skip to content</a>

    
    
    



          <header class="site-header js-details-container" role="banner">
  <div class="container-responsive">
    <a class="header-logo-invertocat" href="https://github.com/" aria-label="Homepage" data-ga-click="(Logged out) Header, go to homepage, icon:logo-wordmark">
      <svg aria-hidden="true" class="octicon octicon-mark-github" height="32" version="1.1" viewBox="0 0 16 16" width="32"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"></path></svg>
    </a>

    <button class="btn-link float-right site-header-toggle js-details-target" type="button" aria-label="Toggle navigation">
      <svg aria-hidden="true" class="octicon octicon-three-bars" height="24" version="1.1" viewBox="0 0 12 16" width="18"><path d="M11.41 9H.59C0 9 0 8.59 0 8c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zm0-4H.59C0 5 0 4.59 0 4c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zM.59 11H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1H.59C0 13 0 12.59 0 12c0-.59 0-1 .59-1z"></path></svg>
    </button>

    <div class="site-header-menu">
      <nav class="site-header-nav site-header-nav-main">
        <a href="/personal" class="js-selected-navigation-item nav-item nav-item-personal" data-ga-click="Header, click, Nav menu - item:personal" data-selected-links="/personal /personal">
          Personal
</a>        <a href="/open-source" class="js-selected-navigation-item nav-item nav-item-opensource" data-ga-click="Header, click, Nav menu - item:opensource" data-selected-links="/open-source /open-source">
          Open source
</a>        <a href="/business" class="js-selected-navigation-item nav-item nav-item-business" data-ga-click="Header, click, Nav menu - item:business" data-selected-links="/business /business/partners /business/features /business/customers /business">
          Business
</a>        <a href="/explore" class="js-selected-navigation-item nav-item nav-item-explore" data-ga-click="Header, click, Nav menu - item:explore" data-selected-links="/explore /trending /trending/developers /integrations /integrations/feature/code /integrations/feature/collaborate /integrations/feature/ship /explore">
          Explore
</a>      </nav>

      <div class="site-header-actions">
            <a class="btn btn-primary site-header-actions-btn" href="/join?source=header-repo" data-ga-click="(Logged out) Header, clicked Sign up, text:sign-up">Sign up</a>
          <a class="btn site-header-actions-btn mr-2" href="/login?return_to=%2FBinPro%2FCONCOCT%2Fblob%2FSTAMPS%2Fdoc%2Fcomplete_example2016.md" data-ga-click="(Logged out) Header, clicked Sign in, text:sign-in">Sign in</a>
      </div>

        <nav class="site-header-nav site-header-nav-secondary">
          <a class="nav-item" href="/pricing">Pricing</a>
          <a class="nav-item" href="/blog">Blog</a>
          <a class="nav-item" href="https://help.github.com">Support</a>
          <a class="nav-item header-search-link" href="https://github.com/search">Search GitHub</a>
              <div class="header-search scoped-search site-scoped-search js-site-search" role="search">
  <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="/BinPro/CONCOCT/search" class="js-site-search-form" data-scoped-search-url="/BinPro/CONCOCT/search" data-unscoped-search-url="/search" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
    <label class="form-control header-search-wrapper js-chromeless-input-container">
      <div class="header-search-scope">This repository</div>
      <input type="text"
        class="form-control header-search-input js-site-search-focus js-site-search-field is-clearable"
        data-hotkey="s"
        name="q"
        placeholder="Search"
        aria-label="Search this repository"
        data-unscoped-placeholder="Search GitHub"
        data-scoped-placeholder="Search"
        autocapitalize="off">
    </label>
</form></div>

        </nav>
    </div>
  </div>
</header>



    <div id="start-of-content" class="accessibility-aid"></div>

      <div id="js-flash-container">
</div>


    <div role="main">
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode">
    <div id="js-repo-pjax-container" data-pjax-container>
      
<div class="pagehead repohead instapaper_ignore readability-menu experiment-repo-nav">
  <div class="container repohead-details-container">

    

<ul class="pagehead-actions">

  <li>
      <a href="/login?return_to=%2FBinPro%2FCONCOCT"
    class="btn btn-sm btn-with-count tooltipped tooltipped-n"
    aria-label="You must be signed in to watch a repository" rel="nofollow">
    <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"></path></svg>
    Watch
  </a>
  <a class="social-count" href="/BinPro/CONCOCT/watchers"
     aria-label="10 users are watching this repository">
    10
  </a>

  </li>

  <li>
      <a href="/login?return_to=%2FBinPro%2FCONCOCT"
    class="btn btn-sm btn-with-count tooltipped tooltipped-n"
    aria-label="You must be signed in to star a repository" rel="nofollow">
    <svg aria-hidden="true" class="octicon octicon-star" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74z"></path></svg>
    Star
  </a>

    <a class="social-count js-social-count" href="/BinPro/CONCOCT/stargazers"
      aria-label="38 users starred this repository">
      38
    </a>

  </li>

  <li>
      <a href="/login?return_to=%2FBinPro%2FCONCOCT"
        class="btn btn-sm btn-with-count tooltipped tooltipped-n"
        aria-label="You must be signed in to fork a repository" rel="nofollow">
        <svg aria-hidden="true" class="octicon octicon-repo-forked" height="16" version="1.1" viewBox="0 0 10 16" width="10"><path d="M8 1a1.993 1.993 0 0 0-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 0 0 2 1a1.993 1.993 0 0 0-1 3.72V6.5l3 3v1.78A1.993 1.993 0 0 0 5 15a1.993 1.993 0 0 0 1-3.72V9.5l3-3V4.72A1.993 1.993 0 0 0 8 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"></path></svg>
        Fork
      </a>

    <a href="/BinPro/CONCOCT/network" class="social-count"
       aria-label="20 users are forked this repository">
      20
    </a>
  </li>
</ul>

    <h1 class="public ">
  <svg aria-hidden="true" class="octicon octicon-repo" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"></path></svg>
  <span class="author" itemprop="author"><a href="/BinPro" class="url fn" rel="author">BinPro</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a href="/BinPro/CONCOCT" data-pjax="#js-repo-pjax-container">CONCOCT</a></strong>

</h1>

  </div>
  <div class="container">
    
<nav class="reponav js-repo-nav js-sidenav-container-pjax"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
     role="navigation"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/BinPro/CONCOCT/tree/STAMPS" aria-selected="true" class="js-selected-navigation-item selected reponav-item" data-hotkey="g c" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches /BinPro/CONCOCT/tree/STAMPS" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-code" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M9.5 3L8 4.5 11.5 8 8 11.5 9.5 13 14 8 9.5 3zm-5 0L0 8l4.5 5L6 11.5 2.5 8 6 4.5 4.5 3z"></path></svg>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a href="/BinPro/CONCOCT/issues" class="js-selected-navigation-item reponav-item" data-hotkey="g i" data-selected-links="repo_issues repo_labels repo_milestones /BinPro/CONCOCT/issues" itemprop="url">
        <svg aria-hidden="true" class="octicon octicon-issue-opened" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M7 2.3c3.14 0 5.7 2.56 5.7 5.7s-2.56 5.7-5.7 5.7A5.71 5.71 0 0 1 1.3 8c0-3.14 2.56-5.7 5.7-5.7zM7 1C3.14 1 0 4.14 0 8s3.14 7 7 7 7-3.14 7-7-3.14-7-7-7zm1 3H6v5h2V4zm0 6H6v2h2v-2z"></path></svg>
        <span itemprop="name">Issues</span>
        <span class="counter">24</span>
        <meta itemprop="position" content="2">
</a>    </span>

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/BinPro/CONCOCT/pulls" class="js-selected-navigation-item reponav-item" data-hotkey="g p" data-selected-links="repo_pulls /BinPro/CONCOCT/pulls" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-git-pull-request" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M11 11.28V5c-.03-.78-.34-1.47-.94-2.06C9.46 2.35 8.78 2.03 8 2H7V0L4 3l3 3V4h1c.27.02.48.11.69.31.21.2.3.42.31.69v6.28A1.993 1.993 0 0 0 10 15a1.993 1.993 0 0 0 1-3.72zm-1 2.92c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zM4 3c0-1.11-.89-2-2-2a1.993 1.993 0 0 0-1 3.72v6.56A1.993 1.993 0 0 0 2 15a1.993 1.993 0 0 0 1-3.72V4.72c.59-.34 1-.98 1-1.72zm-.8 10c0 .66-.55 1.2-1.2 1.2-.65 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"></path></svg>
      <span itemprop="name">Pull requests</span>
      <span class="counter">2</span>
      <meta itemprop="position" content="3">
</a>  </span>


    <a href="/BinPro/CONCOCT/wiki" class="js-selected-navigation-item reponav-item" data-hotkey="g w" data-selected-links="repo_wiki /BinPro/CONCOCT/wiki">
      <svg aria-hidden="true" class="octicon octicon-book" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M3 5h4v1H3V5zm0 3h4V7H3v1zm0 2h4V9H3v1zm11-5h-4v1h4V5zm0 2h-4v1h4V7zm0 2h-4v1h4V9zm2-6v9c0 .55-.45 1-1 1H9.5l-1 1-1-1H2c-.55 0-1-.45-1-1V3c0-.55.45-1 1-1h5.5l1 1 1-1H15c.55 0 1 .45 1 1zm-8 .5L7.5 3H2v9h6V3.5zm7-.5H9.5l-.5.5V12h6V3z"></path></svg>
      Wiki
</a>

  <a href="/BinPro/CONCOCT/pulse" class="js-selected-navigation-item reponav-item" data-selected-links="pulse /BinPro/CONCOCT/pulse">
    <svg aria-hidden="true" class="octicon octicon-pulse" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M11.5 8L8.8 5.4 6.6 8.5 5.5 1.6 2.38 8H0v2h3.6l.9-1.8.9 5.4L9 8.5l1.6 1.5H14V8z"></path></svg>
    Pulse
</a>
  <a href="/BinPro/CONCOCT/graphs" class="js-selected-navigation-item reponav-item" data-selected-links="repo_graphs repo_contributors /BinPro/CONCOCT/graphs">
    <svg aria-hidden="true" class="octicon octicon-graph" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M16 14v1H0V0h1v14h15zM5 13H3V8h2v5zm4 0H7V3h2v10zm4 0h-2V6h2v7z"></path></svg>
    Graphs
</a>

</nav>

  </div>
</div>

<div class="container new-discussion-timeline experiment-repo-nav">
  <div class="repository-content">

    

<a href="/BinPro/CONCOCT/blob/852482878088964026af94a58bfd2249590d70bf/doc/complete_example2016.md" class="d-none js-permalink-shortcut" data-hotkey="y">Permalink</a>

<!-- blob contrib key: blob_contributors:v21:44433d41c64932819cb16b5bb5d2498a -->

<div class="file-navigation js-zeroclipboard-container">
  
<div class="select-menu branch-select-menu js-menu-container js-select-menu float-left">
  <button class="btn btn-sm select-menu-button js-menu-target css-truncate" data-hotkey="w"
    
    type="button" aria-label="Switch branches or tags" tabindex="0" aria-haspopup="true">
    <i>Branch:</i>
    <span class="js-select-button css-truncate-target">STAMPS</span>
  </button>

  <div class="select-menu-modal-holder js-menu-content js-navigation-container" data-pjax aria-hidden="true">

    <div class="select-menu-modal">
      <div class="select-menu-header">
        <svg aria-label="Close" class="octicon octicon-x js-menu-close" height="16" role="img" version="1.1" viewBox="0 0 12 16" width="12"><path d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"></path></svg>
        <span class="select-menu-title">Switch branches/tags</span>
      </div>

      <div class="select-menu-filters">
        <div class="select-menu-text-filter">
          <input type="text" aria-label="Filter branches/tags" id="context-commitish-filter-field" class="form-control js-filterable-field js-navigation-enable" placeholder="Filter branches/tags">
        </div>
        <div class="select-menu-tabs">
          <ul>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="branches" data-filter-placeholder="Filter branches/tags" class="js-select-menu-tab" role="tab">Branches</a>
            </li>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="tags" data-filter-placeholder="Find a tag…" class="js-select-menu-tab" role="tab">Tags</a>
            </li>
          </ul>
        </div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="branches" role="menu">

        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


            <a class="select-menu-item js-navigation-item js-navigation-open selected"
               href="/BinPro/CONCOCT/blob/STAMPS/doc/complete_example2016.md"
               data-name="STAMPS"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                STAMPS
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/SpeedUp/doc/complete_example2016.md"
               data-name="SpeedUp"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                SpeedUp
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/Threaded/doc/complete_example2016.md"
               data-name="Threaded"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                Threaded
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/VGMM_python_alterations/doc/complete_example2016.md"
               data-name="VGMM_python_alterations"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                VGMM_python_alterations
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/Weighted/doc/complete_example2016.md"
               data-name="Weighted"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                Weighted
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/cami/doc/complete_example2016.md"
               data-name="cami"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                cami
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/develop/doc/complete_example2016.md"
               data-name="develop"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                develop
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/fix_kmer_count/doc/complete_example2016.md"
               data-name="fix_kmer_count"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                fix_kmer_count
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/fix_python2.6/doc/complete_example2016.md"
               data-name="fix_python2.6"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                fix_python2.6
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/fix_tests_master/doc/complete_example2016.md"
               data-name="fix_tests_master"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                fix_tests_master
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/fix_tests/doc/complete_example2016.md"
               data-name="fix_tests"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                fix_tests
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/gen_input_table/doc/complete_example2016.md"
               data-name="gen_input_table"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                gen_input_table
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/master/doc/complete_example2016.md"
               data-name="master"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                master
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/normalize_coverage/doc/complete_example2016.md"
               data-name="normalize_coverage"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                normalize_coverage
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/python3conversion/doc/complete_example2016.md"
               data-name="python3conversion"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                python3conversion
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/revert-121-dist_matrix_script/doc/complete_example2016.md"
               data-name="revert-121-dist_matrix_script"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                revert-121-dist_matrix_script
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/testing_docs/doc/complete_example2016.md"
               data-name="testing_docs"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                testing_docs
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/tests_with_clustering.csv/doc/complete_example2016.md"
               data-name="tests_with_clustering.csv"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                tests_with_clustering.csv
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/tests/doc/complete_example2016.md"
               data-name="tests"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                tests
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/travis_tryout/doc/complete_example2016.md"
               data-name="travis_tryout"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                travis_tryout
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/update_documentation/doc/complete_example2016.md"
               data-name="update_documentation"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                update_documentation
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
               href="/BinPro/CONCOCT/blob/variational/doc/complete_example2016.md"
               data-name="variational"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                variational
              </span>
            </a>
        </div>

          <div class="select-menu-no-results">Nothing to show</div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="tags">
        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.4.0/doc/complete_example2016.md"
              data-name="0.4.0"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.4.0">
                0.4.0
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.3.3/doc/complete_example2016.md"
              data-name="0.3.3"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.3.3">
                0.3.3
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.3.2/doc/complete_example2016.md"
              data-name="0.3.2"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.3.2">
                0.3.2
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.3.1/doc/complete_example2016.md"
              data-name="0.3.1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.3.1">
                0.3.1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.3.0/doc/complete_example2016.md"
              data-name="0.3.0"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.3.0">
                0.3.0
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.2.2/doc/complete_example2016.md"
              data-name="0.2.2"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.2.2">
                0.2.2
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.2.1/doc/complete_example2016.md"
              data-name="0.2.1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.2.1">
                0.2.1
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.2.0/doc/complete_example2016.md"
              data-name="0.2.0"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.2.0">
                0.2.0
              </span>
            </a>
            <a class="select-menu-item js-navigation-item js-navigation-open "
              href="/BinPro/CONCOCT/tree/0.1/doc/complete_example2016.md"
              data-name="0.1"
              data-skip-pjax="true"
              rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"></path></svg>
              <span class="select-menu-item-text css-truncate-target" title="0.1">
                0.1
              </span>
            </a>
        </div>

        <div class="select-menu-no-results">Nothing to show</div>
      </div>

    </div>
  </div>
</div>

  <div class="btn-group float-right">
    <a href="/BinPro/CONCOCT/find/STAMPS"
          class="js-pjax-capture-input btn btn-sm"
          data-pjax
          data-hotkey="t">
      Find file
    </a>
    <button aria-label="Copy file path to clipboard" class="js-zeroclipboard btn btn-sm zeroclipboard-button tooltipped tooltipped-s" data-copied-hint="Copied!" type="button">Copy path</button>
  </div>
  <div class="breadcrumb js-zeroclipboard-target">
    <span class="repo-root js-repo-root"><span class="js-path-segment"><a href="/BinPro/CONCOCT/tree/STAMPS"><span>CONCOCT</span></a></span></span><span class="separator">/</span><span class="js-path-segment"><a href="/BinPro/CONCOCT/tree/STAMPS/doc"><span>doc</span></a></span><span class="separator">/</span><strong class="final-path">complete_example2016.md</strong>
  </div>
</div>


  <div class="commit-tease">
      <span class="float-right">
        <a class="commit-tease-sha" href="/BinPro/CONCOCT/commit/852482878088964026af94a58bfd2249590d70bf" data-pjax>
          8524828
        </a>
        <relative-time datetime="2016-08-10T23:28:39Z">Aug 11, 2016</relative-time>
      </span>
      <div>
        <img alt="" class="avatar" data-canonical-src="https://2.gravatar.com/avatar/4bec0958fcc9f962de2c019062cfef84?d=https%3A%2F%2Fassets-cdn.github.com%2Fimages%2Fgravatars%2Fgravatar-user-420.png&amp;r=x&amp;s=140" height="20" src="https://camo.githubusercontent.com/4eb268088b9e27f997ad91faef8d8d860bb381eb/68747470733a2f2f322e67726176617461722e636f6d2f6176617461722f34626563303935386663633966393632646532633031393036326366656638343f643d68747470732533412532462532466173736574732d63646e2e6769746875622e636f6d253246696d6167657325324667726176617461727325324667726176617461722d757365722d3432302e706e6726723d7826733d313430" width="20" />
        <span class="user-mention">Christopher Quince</span>
          <a href="/BinPro/CONCOCT/commit/852482878088964026af94a58bfd2249590d70bf" class="message" data-pjax="true" title="Up">Up</a>
      </div>

    <div class="commit-tease-contributors">
      <button type="button" class="btn-link muted-link contributors-toggle" data-facebox="#blob_contributors_box">
        <strong>0</strong>
         contributors
      </button>
      
    </div>

    <div id="blob_contributors_box" style="display:none">
      <h2 class="facebox-header" data-facebox-id="facebox-header">Users who have contributed to this file</h2>
      <ul class="facebox-user-list" data-facebox-id="facebox-description">
      </ul>
    </div>
  </div>

<div class="file">
  <div class="file-header">
  <div class="file-actions">

    <div class="btn-group">
      <a href="/BinPro/CONCOCT/raw/STAMPS/doc/complete_example2016.md" class="btn btn-sm " id="raw-url">Raw</a>
        <a href="/BinPro/CONCOCT/blame/STAMPS/doc/complete_example2016.md" class="btn btn-sm js-update-url-with-hash">Blame</a>
      <a href="/BinPro/CONCOCT/commits/STAMPS/doc/complete_example2016.md" class="btn btn-sm " rel="nofollow">History</a>
    </div>


        <button type="button" class="btn-octicon disabled tooltipped tooltipped-nw"
          aria-label="You must be signed in to make or propose changes">
          <svg aria-hidden="true" class="octicon octicon-pencil" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path d="M0 12v3h3l8-8-3-3-8 8zm3 2H1v-2h1v1h1v1zm10.3-9.3L12 6 9 3l1.3-1.3a.996.996 0 0 1 1.41 0l1.59 1.59c.39.39.39 1.02 0 1.41z"></path></svg>
        </button>
        <button type="button" class="btn-octicon btn-octicon-danger disabled tooltipped tooltipped-nw"
          aria-label="You must be signed in to make or propose changes">
          <svg aria-hidden="true" class="octicon octicon-trashcan" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"></path></svg>
        </button>
  </div>

  <div class="file-info">
      376 lines (262 sloc)
      <span class="file-info-divider"></span>
    15.1 KB
  </div>
</div>

  
  <div id="readme" class="readme blob instapaper_body">
    <article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-complete-example-v03-stamps-2016" class="anchor" href="#complete-example-v03-stamps-2016" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Complete Example V0.3 STAMPS 2016</h1>

<h1></h1>

<p>This documentation page aims to be a complete example walk through for the usage of the CONCOCT package version 0.3 except for the assembly and COG annotations step.</p>

<p>It is not required to run all steps. The output files for each step are in the test data repository. At the end of this example the results should be the same as the results in the corresponding test data repository. The version numbers listed above are the ones used to generate the results in that repository. Using newer versions will probably not be a problem, but your results may be different in that case.</p>

<h2><a id="user-content-login-to-the-class-servers" class="anchor" href="#login-to-the-class-servers" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Login to the class servers</h2>

<hr>

<pre><code>ssh -X yourname@class.mbl.edu
ssh -X yourname@classxx
</code></pre>

<h2><a id="user-content-setting-up-the-test-environment" class="anchor" href="#setting-up-the-test-environment" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Setting up the test environment</h2>

<hr>

<p>Move to your home directory, create a folder where you want all the output from this example to go:</p>

<pre><code>    cd ~
    mkdir CONCOCT-complete-example
    cd CONCOCT-complete-example
</code></pre>

<p>Set three variables with full paths. One pointing to the root directory of the <code>CONCOCT</code> software, one pointing to the test data repository, named <code>CONCOCT_TEST</code> and one to the directory we just created. </p>

<pre><code>    export CONCOCT=/class/stamps-software/CONCOCT
    export CONCOCT_TEST=/class/stamps-software/CONCOCT-test-data
    export CONCOCT_EXAMPLE=$HOME/CONCOCT-complete-example
</code></pre>

<p>You can see the full path of a directory you are located in by running the command <code>pwd</code>.</p>

<p>Copy in the example data from the class folder:</p>

<pre><code>    cp $CONCOCT_TEST/Example.tar.gz .
</code></pre>

<p>And extract:</p>

<pre><code>    tar -xvzf Example.tar.gz
</code></pre>

<h2><a id="user-content-assembling-metagenomic-reads" class="anchor" href="#assembling-metagenomic-reads" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Assembling Metagenomic Reads</h2>

<hr>

<p>The first step in the analysis is to assemble all reads into contigs, even 
for this small example, 1 million reads per sample and 16 samples, this is computationally 
intensive. There are a number of assemblers available if you want a quick results \megahit generally performs well but Spades is also good. The best choice is data set dependent.</p>

<p>Then assemble the reads. We recommend megahit for this. To perform the assembly I ran the following commands, please <strong>do not run this</strong>:</p>

<pre><code>cd Example 
nohup megahit -1 $(&lt;R1.csv) -2 $(&lt;R2.csv) -t 8 -o Assembly --presets meta &gt; megahit.out&amp;
</code></pre>

<p>However, I <strong>do not</strong> suggest you do this now instead copy the Assembly directory from the class folders:</p>

<pre><code>    cp -r $CONCOCT_TEST/Assembly .
</code></pre>

<h2><a id="user-content-cutting-up-contigs" class="anchor" href="#cutting-up-contigs" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Cutting up contigs</h2>

<hr>

<p>In order to give more weight to larger contigs and mitigate the effect of assembly errors we cut up the contigs into chunks of 10 Kb. The final chunk is appended to the one before it if it is &lt; 10 Kb to prevent generating small contigs. This means that no contig &lt; 20 Kb is cut up. We use the script <code>cut_up_fasta.py</code> for this:</p>

<p>Now lets cut up the contigs and index for the mapping program bwa:</p>

<pre><code>mkdir contigs
python $CONCOCT/scripts/cut_up_fasta.py -c 10000 -o 0 -m $CONCOCT_TEST/Assembly/final.contigs.fa &gt; contigs/final_contigs_c10K.fa
</code></pre>

<h2><a id="user-content-map-the-reads-onto-the-contigs" class="anchor" href="#map-the-reads-onto-the-contigs" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Map the Reads onto the Contigs</h2>

<hr>

<p>After assembly we map the reads of each sample back to the assembly using <a href="https://github.com/lh3/bwa">bwa</a>.</p>

<p>We are not going to perform mapping ourselves. Instead just copy the pre-calculated files:</p>

<pre><code>    cp -r $CONCOCT_TEST/Map .
</code></pre>

<p>These are the commands we ran (<strong>do not run this</strong>).</p>

<pre><code>mkdir Map

for file in Example/*R1.fastq
do 

   stub=${file%_R1.fastq}
   stub2=${stub#Example\/}  
   echo $stub

   file2=${stub}_R2.fastq

   bwa mem -t 4 contigs/final_contigs_c10K.fa $file $file2 &gt; Map/${stub2}.sam
done
</code></pre>

<p>Followed by these (** do not run**):</p>

<pre><code>for file in Map/*.sam
do
    stub=${file%.sam}
    stub2=${stub#Map\/}
    echo $stub  
    samtools view -h -b -S $file &gt; ${stub}.bam
    samtools view -b -F 4 ${stub}.bam &gt; ${stub}.mapped.bam
    samtools sort -m 1000000000 ${stub}.mapped.bam -o ${stub}.mapped.sorted.bam
    bedtools genomecov -ibam ${stub}.mapped.sorted.bam -g contigs/final_contigs_c10K.len &gt; ${stub}_cov.txt
done
</code></pre>

<h2><a id="user-content-generate-coverage-table" class="anchor" href="#generate-coverage-table" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Generate coverage table</h2>

<hr>

<p>Given the processed mapping files we can now generate the coverage table:</p>

<pre><code>$CONCOCT/scripts/Collate.pl $CONCOCT_TEST/Map | tr "," "\t" &gt; Coverage.tsv
</code></pre>

<p>This is a simple tab delimited file with the coverage of each contig per sample.</p>

<h2><a id="user-content-run-concoct" class="anchor" href="#run-concoct" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Run concoct</h2>

<hr>

<p>To see possible parameter settings with a description run</p>

<pre><code>    concoct --help
</code></pre>

<p>We will only run concoct for some standard settings here. The only one we vary is the cluster number which should be at least twice the number of genomes in your 
co-assembly (see discussion below of how to estimate this). In this case we know it is 
around 20 so run concoct with 40 as the maximum number of cluster <code>-c 40</code>:</p>

<pre><code>mkdir Concoct
cd Concoct
mv ../Coverage.tsv .
concoct --coverage_file Coverage.tsv --composition_file ../contigs/final_contigs_c10K.fa
cd ..
</code></pre>

<p>When concoct has finished the message "CONCOCT Finished, the log shows how it went." is piped to stdout. The program generates a number of files in the output directory that can be set with the <code>-b</code> parameter and will be the present working directory by default. </p>

<h2><a id="user-content-contig-annotation" class="anchor" href="#contig-annotation" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Contig annotation</h2>

<p>We are going to annotate COGs on our contigs. You first need to find genes on the contigs and functionally annotate these. Here we used prodigal (<a href="https://github.com/hyattpd/Prodigal">https://github.com/hyattpd/Prodigal</a>) for gene prediction and annotation, but you can use anything you want (<strong>do not run this</strong>):</p>

<pre><code>mkdir Annotate_gt1000
cd Annotate_gt1000
python $CONCOCT/scripts/LengthFilter.py -m 1000 ../contigs/final_contigs_c10K.fa &gt; final_contigs_gt1000_c10K.fa
prodigal -i final_contigs_gt1000_c10K.fa -a final_contigs_gt1000_c10K.faa -d final_contigs_gt1000_c10K.fna  -f gff -p meta -o final_contigs_gt1000_c10K.gff
</code></pre>

<p>Then we assigned COGs (but on another server) - <strong>do not run this</strong></p>

<pre><code>export COGSDB_DIR=/home/opt/rpsblast_db
nohup $CONCOCT/scripts/RPSBLAST.sh -f final_contigs_gt1000_c10K.faa -p -c 32 -r 1 &gt; r.out&amp;
</code></pre>

<p>Instead just copy whole directory into your example dir (do run this)</p>

<pre><code>cd $CONCOCT_EXAMPLE
cp -r $CONCOCT_TEST/Annotate_gt1000 .
</code></pre>

<p>How to determine number of genomes present?</p>

<pre><code>cd Annotate_gt1000
python /class/stamps-software/CONCOCT/scripts/ExtractCOGs.py -b final_contigs_gt1000_c10K.out --cdd_cog_file /class/stamps-software/CONCOCT/scgs/cdd_to_cog.tsv &gt; final_contigs_gt1000_c10K.cogs
$CONCOCT/scripts/CountSCGs.pl $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_generaR.txt &lt; final_contigs_gt1000_c10K.cogs  | cut -d"," -f2 | awk -f $CONCOCT/scripts/median.awk
</code></pre>

<p>The result should be 15, this places an upper limit on the number of genomes we can bin.</p>

<h2><a id="user-content-evaluate-output" class="anchor" href="#evaluate-output" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Evaluate output</h2>

<hr>

<p>This will require that you have Rscript with the R packages <a href="http://cran.r-project.org/web/packages/gplots/index.html">gplots</a>, <a href="http://cran.r-project.org/web/packages/reshape/index.html">reshape</a>, <a href="http://cran.r-project.org/web/packages/ggplot2/index.html">ggplot2</a>, <a href="http://cran.r-project.org/web/packages/ellipse/index.html">ellipse</a>, <a href="http://cran.r-project.org/web/packages/getopt/index.html">getopt</a> and <a href="http://cran.r-project.org/web/packages/grid/index.html">grid</a> installed. The package grid does not have to be installed for R version &gt; 1.8.0</p>

<p>First we can visualise the clusters in the first two PCA dimensions:</p>

<pre><code>cd $CONCOCT_EXAMPLE
mkdir evaluation-output
Rscript $CONCOCT/scripts/ClusterPlot.R -c Concoct/clustering_gt1000.csv -p Concoct/PCA_transformed_data_gt1000.csv -m Concoct/pca_means_gt1000.csv -r Concoct/pca_variances_gt1000_dim -l -o evaluation-output/ClusterPlot.pdf
</code></pre>

<p>To visualise your plots if you have x-windows forwarding just try:</p>

<pre><code>evince evaluation-output/ClusterPlot.pdf
</code></pre>

<p>If that fails you will have to copy them off the server to a local directory. 
Move to that local directory on your computer and type:</p>

<pre><code>scp yourname@class.mbl.edu:~/CONCOCT-complete-example/evaluation-output/ClusterPlot.pdf .
</code></pre>

<p>The figure should look like this:</p>

<p><a href="/BinPro/CONCOCT/blob/STAMPS/doc/figs/ClusterPlot.pdf" target="_blank"><img src="/BinPro/CONCOCT/raw/STAMPS/doc/figs/ClusterPlot.pdf" alt="Cluster PCA" style="max-width:100%;"></a></p>

<p>We can also compare the clustering to species labels. For this test data set we know these labels, they are given in the file <code>$CONCOCT_TEST/AssignGenome/clustering_gt1000_smap.csv</code>. For real data labels may be obtained through taxonomic classification.
In either case we provide a script Validate.pl for computing basic metrics on the cluster quality. Lets copy the validation data into our directory:</p>

<pre><code>cd $CONCOCT_EXAMPLE
cp -r $CONCOCT_TEST/AssignGenome .
</code></pre>

<p>And run our validation script:</p>

<pre><code>cd evaluation-output
$CONCOCT/scripts/Validate.pl --cfile=../Concoct/clustering_gt1000.csv --sfile=../AssignGenome/clustering_gt1000_smap.csv --ffile=../Annotate_gt1000/final_contigs_gt1000_c10K.fa --ofile=clustering_gt1000_conf.csv
</code></pre>

<p>This script requires the clustering output by concoct <code>Concoct/clustering_gt1000.csv</code> these have a simple format of a comma separated file listing each contig id followed by the cluster index and the species labels that have the same format but with a text label rather than a cluster index. The script should output:</p>

<pre><code>N   M   TL  S   K   Rec.    Prec.   NMI Rand    AdjRand
9176    9176    5.8291e+07  20  23  0.986723    0.950877    0.976244    0.993650    0.946975
</code></pre>

<p>This gives the no. of contigs N clustered, the number with labels M, the number of unique labels S, the number of clusters K, the recall, the precision, the normalised mutual information (NMI), the Rand index, and the adjusted Rand index. It also generates a file called a <code>confusion matrix</code> with the frequencies of each species in each cluster. We provide a further script for visualising this as a heatmap:</p>

<pre><code>cd $CONCOCT_EXAMPLE
Rscript $CONCOCT/scripts/ConfPlot.R  -c evaluation-output/clustering_gt1000_conf.csv -o  evaluation-output/clustering_gt1000_conf.pdf
</code></pre>

<p>This generates a file with normalised frequencies of contigs from each cluster across species:</p>

<p><a href="/BinPro/CONCOCT/blob/STAMPS/doc/figs/clustering_gt1000_conf.pdf" target="_blank"><img src="/BinPro/CONCOCT/raw/STAMPS/doc/figs/clustering_gt1000_conf.pdf" alt="Confusion matrix" style="max-width:100%;"></a></p>

<p>To view this also download off server to your local directory:</p>

<pre><code>scp yourname@class.mbl.edu:~/CONCOCT-complete-example/evaluation-output/clustering_gt1000_conf.pdf .
</code></pre>

<h2><a id="user-content-validation-using-single-copy-core-genes" class="anchor" href="#validation-using-single-copy-core-genes" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Validation using single-copy core genes</h2>

<hr>

<p>We can also evaluate the clustering based on single-copy core genes. We will use our results from above in <code>Annotate_gt1000</code> to do this.</p>

<pre><code>cd $CONCOCT_EXAMPLE 
$CONCOCT/scripts/COG_table.py -b Annotate_gt1000/final_contigs_gt1000_c10K.out -m $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_genera.txt -c  Concoct/clustering_gt1000.csv --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv &gt; evaluation-output/clustering_gt1000_scg.tab
</code></pre>

<p>The script requires the clustering output by concoct <code>concoct-output/clustering_gt1000.csv</code>, a file listing a set of SCGs (e.g. a set of COG ids) to use <code>scgs/scg_cogs_min0.97_max1.03_unique_genera.txt</code> and a mapping of Conserved Domain Database ids (<a href="https://www.ncbi.nlm.nih.gov/Structure/cdd/cdd.shtml">https://www.ncbi.nlm.nih.gov/Structure/cdd/cdd.shtml</a>) to COG ids <code>$CONCOCT/scgs/cdd_to_cog.tsv</code>.</p>

<p>The output file is a tab-separated file with basic information about the clusters (cluster id, ids of contigs in cluster and number of contigs in cluster) in the first three columns, and counts of the different SCGs in the following columns.</p>

<p>This can also be visualised graphically using the R script:</p>

<pre><code>cd $CONCOCT_EXAMPLE
Rscript $CONCOCT/scripts/COGPlot.R -s evaluation-output/clustering_gt1000_scg.tab -o evaluation-output/clustering_gt1000_scg.pdf
</code></pre>

<p>To view this also download off server to your local directory:</p>

<pre><code>scp yourname@class.mbl.edu:~/CONCOCT-complete-example/evaluation-output/clustering_gt1000_scg.pdf .
</code></pre>

<p>The plot is downloadable here:</p>

<p><a href="/BinPro/CONCOCT/blob/STAMPS/doc/figs/clustering_gt1000_scg.pdf" target="_blank"><img src="/BinPro/CONCOCT/raw/STAMPS/doc/figs/clustering_gt1000_scg.pdf" alt="scg plot" style="max-width:100%;"></a></p>

<p>How many 75% complete genomes did we get. Do this yourselves in R.</p>

<pre><code>R
&gt; scg &lt;- read.table("clustering_gt1000_scg.tab",header=TRUE,row.names=1)
&gt; scg &lt;- scg[,-1]
&gt; scg &lt;- scg[,-1]
&gt;sum(rowSums(scg == 1)/36. &gt; 0.75)
&gt;q()
</code></pre>

<p>We got 13 75% complete genomes.</p>

<h2><a id="user-content-comparison-to-metabat" class="anchor" href="#comparison-to-metabat" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Comparison to MetaBat</h2>

<p>We will also compare to a competitor algorithm released last year <a href="https://bitbucket.org/berkeleylab/metabat">MetaBat</a> and 
<a href="https://peerj.com/articles/1165/">paper</a>. Note the claim 
"MetaBAT outperforms alternative methods in accuracy and computational efficiency on both synthetic and real metagenome datasets.".</p>

<pre><code>module load metabat
mkdir Metabat
cd Metabat
runMetaBat.sh -m 1500 ../contigs/final_contigs_c10K.fa ../Map/Sample*_sub.bam
</code></pre>

<p>We run it on the same contigs utilising the same bam files. The minimum length that MetaBat will allow is 1500bp. So once this is done to provide a fair comparison we will 
also rerun CONCOCT with this minimum contig length.</p>

<pre><code>cd $CONCOCT_EXAMPLE
mkdir Concoct_gt1500
concoct --coverage_file ../Concoct/Coverage.tsv --composition_file ../contigs/final_contigs_c10K.fa -c 40 -l 1500
</code></pre>

<p>Lets compare the Metabat results with CONCOCT. First we maninpulate the cluster assignments into our format:</p>

<pre><code>cd $CONCOCT_EXAMPLE/Metabat
grep "&gt;" final_contigs_c10K.fa.metabat-bins*fa | sed 's/.fa:&gt;/,/g' | sed 's/final_contigs_c10K.fa.metabat-bins-_-m_1500\.//g' | awk -F, '{print $2,$1}' OFS=, &gt; clustering_gt1500.csv
</code></pre>

<p>Then we run the validation script:</p>

<pre><code> $CONCOCT/scripts/Validate.pl --cfile=clustering_gt1500.csv --sfile=../AssignGenome/clustering_gt1000_smap.csv --ffile=../Annotate_gt1000/final_contigs_gt1000_c10K.fa --ofile=clustering_gt1500_conf.csv
</code></pre>

<pre><code>N   M   TL  S   K   Rec.    Prec.   NMI Rand    AdjRand
6649    6649    5.2942e+07  17  29  0.872325    0.999852    0.937318    0.984568    0.868407
</code></pre>

<p>We can also generate confusion plots and the the SCG table..</p>

<pre><code>$CONCOCT/scripts/COG_table.py -b ../Annotate_gt1000/final_contigs_gt1000_c10K.out -m $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_genera.txt -c clustering_gt1500.csv --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv &gt; clustering_gt1500_scg.tab

Rscript $CONCOCT/scripts/COGPlot.R -s clustering_gt1500_scg.tab -o metabat_clustering_gt1500_scg.pdf

Rscript $CONCOCT/scripts/ConfPlot.R  -c clustering_gt1500_conf.csv -o metabat_clustering_gt1500_conf.pdf
</code></pre>

<p>To generate:</p>

<p><a href="/BinPro/CONCOCT/blob/STAMPS/doc/figs/metabat_clustering_gt1500_scg.pdf" target="_blank"><img src="/BinPro/CONCOCT/raw/STAMPS/doc/figs/metabat_clustering_gt1500_scg.pdf" alt="Metabat scg plot" style="max-width:100%;"></a></p>

<p><a href="/BinPro/CONCOCT/blob/STAMPS/doc/figs/metabat_clustering_gt1500_conf.pdf" target="_blank"><img src="/BinPro/CONCOCT/raw/STAMPS/doc/figs/metabat_clustering_gt1500_conf.pdf" alt="Metabat conf plot" style="max-width:100%;"></a></p>

<p>These confirm that Metabat suffers from fragmentation errors. In fact we get 11 75% complete genomes.</p>

<p>We can compare to CONCOCT at the same contig cut-off:</p>

<pre><code>cd $CONCOCT_EXAMPLE
cd Concoct_gt1500
$CONCOCT/scripts/Validate.pl --cfile=clustering_gt1500.csv --sfile=../AssignGenome/clustering_gt1000_smap.csv --ffile=../Annotate_gt1000/final_contigs_gt1000_c10K.fa --ofile=clustering_gt1500_conf.csv
</code></pre>

<pre><code>N   M   TL  S   K   Rec.    Prec.   NMI Rand    AdjRand
7092    7092    5.5752e+07  20  21  0.996269    0.985881    0.991647    0.999236    0.993561
</code></pre>

<p>Substantially better. Looking at SCGs...</p>

<pre><code>$CONCOCT/scripts/COG_table.py -b ../Annotate_gt1000/final_contigs_gt1000_c10K.out -m $CONCOCT/scgs/scg_cogs_min0.97_max1.03_unique_genera.txt -c clustering_gt1500.csv --cdd_cog_file $CONCOCT/scgs/cdd_to_cog.tsv &gt; clustering_gt1500_scg.tab
Rscript $CONCOCT/scripts/COGPlot.R -s clustering_gt1500_scg.tab -o concoct_clustering_gt1500_scg.pdf
Rscript $CONCOCT/scripts/ConfPlot.R  -c clustering_gt1500_conf.csv -o concoct_clustering_gt1500_conf.pdf
</code></pre>

<p>Now we have 14. Here are the plots..</p>

<p><a href="/BinPro/CONCOCT/blob/STAMPS/doc/figs/concoct_clustering_gt1500_scg.pdf" target="_blank"><img src="/BinPro/CONCOCT/raw/STAMPS/doc/figs/concoct_clustering_gt1500_scg.pdf" alt="CONCOCT scg plot" style="max-width:100%;"></a></p>

<p><a href="/BinPro/CONCOCT/blob/STAMPS/doc/figs/concoct_clustering_gt1500_conf.pdf" target="_blank"><img src="/BinPro/CONCOCT/raw/STAMPS/doc/figs/concoct_clustering_gt1500_conf.pdf" alt="CONCOCT conf plot" style="max-width:100%;"></a></p>
</article>
  </div>

</div>

<button type="button" data-facebox="#jump-to-line" data-facebox-class="linejump" data-hotkey="l" class="d-none">Jump to Line</button>
<div id="jump-to-line" style="display:none">
  <!-- </textarea> --><!-- '"` --><form accept-charset="UTF-8" action="" class="js-jump-to-line-form" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
    <input class="form-control linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
    <button type="submit" class="btn">Go</button>
</form></div>

  </div>
  <div class="modal-backdrop js-touch-events"></div>
</div>


    </div>
  </div>

    </div>

        <div class="container site-footer-container">
  <div class="site-footer" role="contentinfo">
    <ul class="site-footer-links float-right">
        <li><a href="https://github.com/contact" data-ga-click="Footer, go to contact, text:contact">Contact GitHub</a></li>
      <li><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
      <li><a href="https://shop.github.com" data-ga-click="Footer, go to shop, text:shop">Shop</a></li>
        <li><a href="https://github.com/blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a href="https://github.com/about" data-ga-click="Footer, go to about, text:about">About</a></li>

    </ul>

    <a href="https://github.com" aria-label="Homepage" class="site-footer-mark" title="GitHub">
      <svg aria-hidden="true" class="octicon octicon-mark-github" height="24" version="1.1" viewBox="0 0 16 16" width="24"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"></path></svg>
</a>
    <ul class="site-footer-links">
      <li>&copy; 2016 <span title="0.06077s from github-fe158-cp1-prd.iad.github.net">GitHub</span>, Inc.</li>
        <li><a href="https://github.com/site/terms" data-ga-click="Footer, go to terms, text:terms">Terms</a></li>
        <li><a href="https://github.com/site/privacy" data-ga-click="Footer, go to privacy, text:privacy">Privacy</a></li>
        <li><a href="https://github.com/security" data-ga-click="Footer, go to security, text:security">Security</a></li>
        <li><a href="https://status.github.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a href="https://help.github.com" data-ga-click="Footer, go to help, text:help">Help</a></li>
    </ul>
  </div>
</div>



    

    <div id="ajax-error-message" class="ajax-error-message flash flash-error">
      <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M8.865 1.52c-.18-.31-.51-.5-.87-.5s-.69.19-.87.5L.275 13.5c-.18.31-.18.69 0 1 .19.31.52.5.87.5h13.7c.36 0 .69-.19.86-.5.17-.31.18-.69.01-1L8.865 1.52zM8.995 13h-2v-2h2v2zm0-3h-2V6h2v4z"></path></svg>
      <button type="button" class="flash-close js-flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
        <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"></path></svg>
      </button>
      You can't perform that action at this time.
    </div>


      <script crossorigin="anonymous" src="https://assets-cdn.github.com/assets/compat-40e365359d1c4db1e36a55be458e60f2b7c24d58b5a00ae13398480e7ba768e0.js"></script>
      <script crossorigin="anonymous" src="https://assets-cdn.github.com/assets/frameworks-f2534631b1ca6bf10c7effe73f9786cc1fb3426f2674a91519497864b6648282.js"></script>
      <script async="async" crossorigin="anonymous" src="https://assets-cdn.github.com/assets/github-a87b249a8cd99dc3cc1181de10363bf4977348a01f2cc65cd08a0e6af5550176.js"></script>
      
      
      
      
      
      
    <div class="js-stale-session-flash stale-session-flash flash flash-warn flash-banner d-none">
      <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path d="M8.865 1.52c-.18-.31-.51-.5-.87-.5s-.69.19-.87.5L.275 13.5c-.18.31-.18.69 0 1 .19.31.52.5.87.5h13.7c.36 0 .69-.19.86-.5.17-.31.18-.69.01-1L8.865 1.52zM8.995 13h-2v-2h2v2zm0-3h-2V6h2v4z"></path></svg>
      <span class="signed-in-tab-flash">You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
      <span class="signed-out-tab-flash">You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
    </div>
    <div class="facebox" id="facebox" style="display:none;">
  <div class="facebox-popup">
    <div class="facebox-content" role="dialog" aria-labelledby="facebox-header" aria-describedby="facebox-description">
    </div>
    <button type="button" class="facebox-close js-facebox-close" aria-label="Close modal">
      <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"></path></svg>
    </button>
  </div>
</div>

  </body>
</html>

