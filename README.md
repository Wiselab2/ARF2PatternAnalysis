###### <div align="right"> Author: Priyanka Surana </div> <div align="right"> Plant Breeding Institute, University of Sydney </div>

### <div align="center"> Identifying Genes With ARF2-like Expression Pattern </div> 

This data set utilizes barley transcriptome sequenced and quantified for wildtype (*Mla6*) and mutant (*mla6*) at 6 timepoints (0, 16, 20, 24, 32 and 48 hours after infection) for 3 replications. ARF2 (HORVU5Hr1G111500) like genes are identified using expression pattern analysis.

1. Normalized Read Counts
Salmon (Patro et al. 2017) was used to quantify gene-counts using genome alignments from STAR (Patro et al. 2017). Count normalization was done in a taxon-specific manner, as described in (Klingenberg and Meinicke 2017). Normalized read counts are used to calculate averages and standard error for each genotype x timepoint combination.

2. Include Annotation, Differential Expression and Log2 Fold Change Data
Annotation performed using InterProScan (Jones et al. 2014) is read along with differential expression and log2 fold change data. Differential expression was performed using using R package DESeq2 in Bioconductor (Love et al. 2014). 

3. eQTL Data
Expression quantitative trait loci (eQTL) information was downloaded from Surana et al. 2017.

4. Remove High Standard Error Genes
A gene with a standard error greater than 1 for any genotype x timepoint combination is removed.

5. Pattern Analysis
A gene with an adjusted p-value of less than or equal to 0.001 and log2 fold change of greater than 1 at 20 HAI is considered significant. For the other timepoints, the log2 fold change values must less than 0.5 but greater than -0.5.

6. Remove Low Read Count Genes
A gene with a read count of less than or equal to 10 for any genotype x timepoint combination is removed.

7. Repeat Pattern Analysis
Step (5) is repeated but without low read count genes.
