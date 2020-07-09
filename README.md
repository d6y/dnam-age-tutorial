# DNAm Age Tutorial

This repository contains variation of the "R Tutorials" software at: 
https://horvath.genetics.ucla.edu/html/dnamage/

> "[...] the original standard analysis is implemented in the following R software tutorial
> that shows how to calculate DNAm age based on Illumina DNA Infinium 27K or 450K data is available. 
> These R scripts carry out normalization steps and show how to estimate DNAm age."

Based on the number of CpG sites selected (`AdditionalFile3.csv`),
I believe this code corresponds to the work in: 

Horvath, S. _DNA methylation age of human tissues and cell types_. Genome Biol 14, 3156 (2013). https://doi.org/10.1186/gb-2013-14-10-r115

# First time set up

This step installs dependencies (it takes a while to compile up the binaries).
You'll need R and development tools (probably gcc).

```
$ R
> if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
> BiocManager::install()
> BiocManager::install("impute")
> BiocManager::install("preprocessCore")
> BiocManager::install("GO.db")
> BiocManager::install("AnnotationDbi")
> BiocManager::install("RPMM")
> install.packages("sqldf")
> install.packages("WGCNA")
```

# Run

```
$ R
> source("main.r")
```

I used R version 4.0.2.

