###### <div align="right"> Author: Priyanka Surana </div> <div align="right"> Plant Breeding Institute, University of Sydney </div>

### <div align="center"> Identifying Genes With ARF2-like Expression Pattern </div> 

This data set utilizes barley transcriptome sequenced and quantified for wildtype (*Mla6*) and mutant (*mla6*) at 6 timepoints for 3 replications.

1. Normalized Read Counts
Salmon (Patro et al. 2017) was used to quantify gene-counts using genome alignments from STAR (Patro et al. 2017). Count normalization was done in a taxon-specific manner, as described in (Klingenberg and Meinicke 2017). Normalized read counts are used to calculate averages and standard error for each genotype x timepoint combination.

2. Include Annotation, Differential Expression and Log2 Fold Change Data
Annotation performed using InterProScan (Jones et al. 2014) is read along with differential expression and log2 fold change data. Differential expression was performed using using R package DESeq2 in Bioconductor (Love et al. 2014). 

3. eQTL Data
Expression quantitative trait loci (eQTL) information was downloaded from Surana et al. 2017.

4. Remove High Standard Error Genes


5. Pattern Analysis

6. Remove Low Read Count Genes

7. Repeat Pattern Analysis
