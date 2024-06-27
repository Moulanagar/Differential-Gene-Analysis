# Differential-Gene-Analysis

**Differential gene expression (DGE) analysis** is commonly used in the transcriptome-wide analysis (using RNAseq) 
for studying the changes in gene or transcripts expressions under different conditions (e.g. control vs infected). 
RNA sequencing (bulk and single-cell RNA-seq) using next-generation sequencing (e.g. Illumina short-read 
sequencing) is a de facto method for quantifying the transcriptome-wide gene or transcript expressions and 
performing DGE analysis. There are several computational tools are available for Differential gene expression 
analysis. In this project, we will DESeq2 for DGE analysis on our dataset.

**DESeq2** requires raw integer read counts for performing accurate DGE analysis. The normalized read counts 
should not be used in DESeq2 analysis. DESeq2 internally normalizes the count data correcting for differences in 
the library sizes as sequencing depth influence the read counts (sample-specific effect). DESeq2 does not 
consider gene length for normalization as gene length is constant for all samples (it may not have significant 
effect on DGE analysis). [1]. Given below is a standard pipeline for RNA sequencing
