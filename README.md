
# Usage <br>

The R script to perform the main part (Fisher’s exact test) of PoTRA, the alternative part (K.S. test) of PoTRA, and the overlay plot of kernel density for the PR scores: <b>PoTRA.R</b><br>

Example usage of PoTRA.R: <b>PoTRA-example.R</b><br>

Data used in PoTRA-example.R: <b>PoTRA-example-data.Rdata</b><br>


library(BiocGenerics) <br>
library(graph) <br>
library(graphite) <br>
library(igraph) <br>

<b>Choose your database before running the PoTRA.cor commandline: <br> </b>
<code>humanKEGG <- pathways("hsapiens", "kegg") </code>


<b>For PoTRA (Fisher’s exact test and K.S. test) based on correlation networks:</b> <br>

<code>PoTRA.cor <- function(mydata,genelist,Num.sample.normal,Num.sample.case,Pathway.database, PR.quantile)</code>
 
<b>Example Usage: </b><br>
<code>results.cor <-PoTRA.cor(mydata=mydata,genelist=genelist,Num.sample.normal=8,Num.sample.case=8,Pathway.database=humanKEGG[1:10],PR.quantile=0.95)</code>


<b>For PoTRA (Fisher’s exact test and K.S. test) based on combined networks:</b> <br>

<code>PoTRA.comb <- function(mydata,genelist,Num.sample.normal,Num.sample.case,Pathway.database)</code>

<b>Example Usage: </b><br>
<code>results.comb <-PoTRA.comb(mydata=mydata,genelist=genelist,Num.sample.normal=8,Num.sample.case=8,Pathway.database=humanKEGG[1:10],PR.quantile=0.95)</code>


<b>For the kernel density plot:</b> <br>

<code>results.plot <- overlayplot(mydata,genelist,Num.sample.normal,Num.sample.case,Pathway.database)</code>

 
<b>Example Usage: </b><br>

<code>results.plot <- overlayplot(mydata=mydata,genelist=genelist,Num.sample.normal=8,Num.sample.case=8,Pathway.database=humanKEGG[[1]])</code>

# Arguments

<html>
