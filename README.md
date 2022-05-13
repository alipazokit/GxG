# GxG
 Efficient GxG estimator

## Prerequisites
The following packages are required on a linux machine to compile and use the software package.
```
g++ (4.4.7)
cmake
make
```

## How to install :

```
git clone https://github.com/alipazokit/GxG.git
cd GxG
mkdir build
cd build/
cmake ..
make
```

## Parameters

```
genotype (-g) : The path of genotype file
annotation (-annot): The path of annotation file.
num_block (-jn): The number of stream blocks. (the higher number of blocks, the lower memory usage)
out_put (-o): The path of output file.


```
## File formats
```
Genotype : It must be in bed format.
Annotation: It has M rows (M=number  of SNPs) and 3 columns.

First column corresponds to SNPs with additive effect. 

Second and third column correspond to two groups of SNPs which have interaction with each other (there is no interaction inside each group). Third (group)column is assumed to be  smaller than second.

If SNP i belongs to annotation j, then there is  "1" in row i and column j. Otherwise there is "0". (delimiter is " ")






