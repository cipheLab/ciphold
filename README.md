# CIPHoLD : Adaptation of the SCAFFOLD cytometry tool.
<h2> Install dependencies </h2>
To use this tool you need a windows computer with :
<ul>
  <li>R version 3.5.1 or later </li>
  <li>R studio </li>
  <li>R tools 3.5 (administrator installation and check "Path environment" box during installation)</li>
  <li>Google Chrome browser (to download zip output correctly)</li>
</ul>
<p>Now run your Rstudio and you can copy paste this commande line to install all apcajges requierd by CIPHoLD tools: </p>

```
  install.packages(c("devtools","shiny","shinydashboard","shinyjs","gtools","shinyHeatmaply"))
  install.packages("lme4")
  install.packages("BiocManager")
  BiocManager::install("flowCore", version = "3.8")
  BiocManager::install("ggcyto", version = "3.8")
  library("devtools")
  install_github("cipheLab/CIPHoLD")
```

<h2> Run Tool </h2>

```
  library("CIPHoLD")
  CIPHoLD.run()
```

<h2> Presentation </h2>
<h4>Lexical</h4>
<ul>
  <li>Over-clustering : Its a volontaryto ask more cluster than population expected with unsupervised algorithme. With that you can play like a downsampling data which each cluster is a heterogenous cell groups (its not a population, we don't have this information).This approch it's used in SPADE, FlowSOM and other clustering algorithme </li>
  <li>Enrichment : </li>
  <li>Annotation : </li>
</ul>

CIPHoLD Tools is a rewrite of SCAFFOLD tools (https://github.com/nolanlab/scaffold). 
<ul> <h4>Difference with scaffold</h4> 
  <li> File manager </li>
  <li> Upload CSV file (clustering from other tools) </li>
  <li> Add other clustering method </li>
  <li> Write annotation in FCS files </li>
  <li> All interface update with dashboard </li>
  <li> Different output format and information </li>
</ul>
We decide to change the input and output system. 

<h2> Upload Data </h2>

<p>You can upload FCS in first tab and create group. Group creation is just a concatenation of FCS with new parameters used to save the files id (sample)</p>

<img src="https://raw.githubusercontent.com/cipheLab/CIPHoLD/master/doc/img/01.png" width=700px/>

<p> upload your multiple fcs file , you can upload 5G of data, if you can't make a issu or send mail and we change this option.</p>

<img src="https://raw.githubusercontent.com/cipheLab/CIPHoLD/master/doc/img/02.png" width=700px/>

<p>You can create one groupe by file or concantenate multiple file (sample) in one. Its a good idea to donc change the cluster position 
 in forced-directe-graph and just view a size cluster changing</p>

<img src="https://raw.githubusercontent.com/cipheLab/CIPHoLD/master/doc/img/03.png" width=700px/>

<p></p>

<img src="https://raw.githubusercontent.com/cipheLab/CIPHoLD/master/doc/img/04.png" width=700px/>

<p>You can upload csv table, with this files you don't need to clustering. Its result of clustering parts </p>
  
 <h2> Clustering </h2>
 
 <p>The clustering is an over-clustering. You need ask more than 100 clusters to make works the annotation. With CIPHoLD you can use gated file from one technology (flow, mass, rnaseq, etc..) for create map and annotate fcs file from other technology, because you can use different transformation on clustered file and gated files.</p>
 
 <img src="https://raw.githubusercontent.com/cipheLab/CIPHoLD/master/doc/img/05.png" >
 
 <p> 1 : a : Select transform function you want use, arcsinh (masse data with 5 in argument or 150 for flow data) or logicle transform with biexp arg (value below zero save in fcs as $PnW keyword for each parameters </p>
 <p> 1 : b : Select argument in transform function and compensate or not. If its mass data and they are no "SPILL"keyword automaticly compensate a not engage.
 <p> 1 : c : If you don't want transform value, like clustering enrichment, annotaion, t-sne coordinate, or other reduction dimensions or information, its possible to "safe" your parameters in this part</p>
 <p> 2 : a : If you upad enriched fcss wih over-cspas in expression matrce, you need to select this params in this field. Don't forget, if it's necessary, to transform other value and don't transforrm your enrichment parameters </p>
 <p> 3 : a : </p>
 
 
 <h2> Gated Files and Map creation </h2>
 
 
 <h2> Map new dataset </h2>
 
 
 <h2> Explore Mapping </h2>
 
 
 <h2> Download Annotation </h2>
 
 
 
