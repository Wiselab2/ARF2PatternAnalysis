###### <div align="right"> Author: Priyanka Surana </div> <div align="right"> Plant Breeding Institute, University of Sydney </div>

### <div align="center"> Identifying Genes With ARF2-like Expression Pattern </div> 

The work here is done for "Manuscript Title" by Authors.

This data set utilizes barley transcriptome sequenced and quantified for wildtype (*Mla6*) and mutant (*mla6*) at 6 timepoints (0, 16, 20, 24, 32 and 48 hours after infection) for 3 replications. ARF2 (HORVU5Hr1G111500) like genes are identified using expression pattern analysis.

**Normalized Read Counts**
</br> Salmon (Patro *et al.* 2017) was used to quantify gene-counts using genome alignments from STAR (Dobin *et al.* 2013). Count normalization was done in a taxon-specific manner, as described in Klingenberg and Meinicke 2017. Log2 of normalized read counts are used to calculate averages and standard error for each genotype x timepoint combination.

**Include Annotation, Differential Expression and Log2 Fold Change Data**
</br> Annotation performed using InterProScan (Jones *et al.* 2014) is read along with differential expression and log2 fold change data. Differential expression was performed using using R package DESeq2 in Bioconductor (Love *et al.* 2014). 

**eQTL Data**
</br> Expression quantitative trait loci (eQTL) information was obtained from Surana et al. 2017.

**Remove High Standard Error Genes**
</br> A gene with a standard error greater than 1 for any genotype x timepoint combination is removed.

**Pattern Analysis**
</br> A gene with an adjusted p-value of less than or equal to 0.001 and log2 fold change of greater than 1 at 20 HAI is considered significant. For the other timepoints, the log2 fold change values must less than 0.5 but greater than -0.5.

**Remove Low Read Count Genes**
</br> A gene with a read count of less than or equal to 10 for any genotype x timepoint combination is removed.

**Repeat Pattern Analysis**
</br> Step (5) is repeated but without low read count genes.

----

**_Citations_**
</br> Patro R, Duggal G, Love MI, Irizarry RA, Kingsford C. Salmon provides fast and bias-aware quantification of transcript expression. Nat Methods. 2017 Apr;14(4):417-419. doi: 10.1038/nmeth.4197. Epub 2017 Mar 6. PubMed PMID: 28263959; PubMed Central PMCID: PMC5600148.

Dobin A, Davis CA, Schlesinger F, Drenkow J, Zaleski C, Jha S, Batut P, Chaisson M, Gingeras TR. STAR: ultrafast universal RNA-seq aligner. Bioinformatics. 2013 Jan 1;29(1):15-21. doi: 10.1093/bioinformatics/bts635. Epub 2012 Oct 25. PubMed PMID: 23104886; PubMed Central PMCID: PMC3530905.

Klingenberg H, Meinicke P. How to normalize metatranscriptomic count data for differential expression analysis. PeerJ. 2017 Oct 17;5:e3859. doi:10.7717/peerj.3859. eCollection 2017. PubMed PMID: 29062598; PubMed Central PMCID: PMC5649605.

Jones P, Binns D, Chang HY, Fraser M, Li W, McAnulla C, McWilliam H, Maslen J, Mitchell A, Nuka G, Pesseat S, Quinn AF, Sangrador-Vegas A, Scheremetjew M, Yong SY, Lopez R, Hunter S. InterProScan 5: genome-scale protein function classification. Bioinformatics. 2014 May 1;30(9):1236-40. doi:10.1093/bioinformatics/btu031. Epub 2014 Jan 21. PubMed PMID: 24451626; PubMed Central PMCID: PMC3998142.

Love MI, Huber W, Anders S. Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2. Genome Biol. 2014;15(12):550. PubMed PMID:25516281; PubMed Central PMCID: PMC4302049.

Surana P, Xu R, Fuerst G, Chapman AVE, Nettleton D, Wise RP. Interchromosomal Transfer of Immune Regulation During Infection of Barley with the Powdery Mildew Pathogen. G3 (Bethesda). 2017 Oct 5;7(10):3317-3329. doi: 10.1534/g3.117.300125. PubMed PMID: 28790145; PubMed Central PMCID: PMC5633382.
