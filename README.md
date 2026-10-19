# CoDA-and-PCA-plots
Compositional Data Analysis (CoDA) of 16S rRNA amplicon data and PCA plotting (biplot and individuals) uisng the package factoextra. R Markdown file was produced using a modified code listed in the tutorial by [Gloor (2016) ](https://utoronto.scholaris.ca/server/api/core/bitstreams/3e157769-5e22-40c7-bb72-12e984afc242/content)for CoDA. Principal Coordinate Analysis (PCA) was ran using [factoextra tutorial (ver.2.2.0.9000)](https://rpkgs.datanovia.com/factoextra/). 

# Installation
Note: R version 4.5.1 and R Studio version 2025.09.0 were used to create and run the R Markdown file. To be able to certain download packages from the listed Bioconductor version, it requires R version 4.5 or greater.

The following packages were used:
[phyloseq](https://joey711.github.io/phyloseq/) (from Bioconductor version 3.21) (will be used to import, store, analyze large and complex sequencing datasets):
```{}
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("phyloseq", version = "3.21")
```
Biostrings (from Bioconductor version 3.21) (will be used for table manipulation of large biological sequences or sets of sequences):
```{}
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("Biostrings", version = "3.21")
```

tidyverse (version 2.0.0 was used) (will be used for table manipulation and viewing):
```{}
install.packages ("tidyverse")
```

reshape2 (version 1.4.4 was used) (will be used for table manipulation):
```{}
install.packages ("reshape2")
```

compositions (version 2.0-9 was used) (will be used in CoDA):
```{}
install.packages ("compositions")
```

ALDEx2 (from Bioconductor version 3.21) (will be used in CoDA):
```{}
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("ALDEx2", version = "3.21")
```

FactoMineR (version 2.14 was used) (will be used in PCA):
```{}
install.packages ("FactoMineR")
```
factoextra (version 2.0.0 was used) (will be used in PCA):
```{}
install.packages ("factoextra")
```

# How to Use
Download R Markdown file to access script. Will need post-processing 16S rRNA amplicon sequencing data (e.g., through the DADA2 pipeline) and in the proper format to be converted as a phyloseq object. Please modify to file paths/data needs (an example is shown within the script).

# Output
Will process 16S rRNA amplicon sequencing data through CoDA analysis and then will perform PCA at the genus level to evaluate differences in beta diversity (in relation to sample location and date) and assess community drivers in differences in variation. 
