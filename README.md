## Utilities for RNA-seq analyses

This repository contains a collection of modules for RNA-seq analyses:
* `annotation`: module for representing and working with gene annotations in [GTF format](https://www.gencodegenes.org/pages/data_format.html).
* `rnaseqnorm`: collection of functions for RNA-seq normalization, including DESeq size factors ([Anders & Huber, 2010](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2010-11-10-r106)) and TMM ([Robinson & Oshlack, 2010](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2010-11-3-r25)).

### Install
Clone this repository:
```
git clone git@github.com:francois-a/rnaseq-utils.git
```
Add the repository to your Python path:
```
export PYTHONPATH=$PYTHONPATH:/<path_to>/rnaseq-utils
```

### Examples
Download the GENCODE 30 GTF:
```
wget ftp://ftp.ebi.ac.uk/pub/databases/gencode/Gencode_human/release_30/gencode.v30.annotation.gtf.gz
```
Load annotation
```
import annotation
annot = annotation.Annotation('gencode.v30.annotation.gtf.gz')
```
Get gene by HGNC symbol:
```
gene = annot.get_gene('MYL9')
```
Display information:
```
print(gene)
````
