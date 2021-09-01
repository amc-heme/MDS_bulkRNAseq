# MDS_rstudio
an Rstudio document to process all the MDS_bulk_RNAseq data

This document is looking at the analysis of the original 9 samples of the MDS bulk RNAseq data from Brett Stevens.  This data was collected on 07/21/15, 09/14/14 
and 12/03/14.  There are 3 patients that each have 3 samples: Bulk, CD123-, CD123+.  These samples were prepared with the Illumina Truseq protoocol.  
They are unstranded and SE100 bp.  The data were analyzed with FASTP, trimmed with cutadapt using the Truseq adapter and aligned with Salmon v1.3.0 and STAR 2.7.9a using the human gencode V38 genome.

For the first round of analysis I ran both unfilter and filtered data with an rMIn of 5 reads per sample.  For the unfiltered data we were seeing that a lot of our differentially expressed data had low counts which is not ideal due to it being more likely to just be caused by sequencing variation etc.  When we required 5 reads per gene per sample we filtered out ~75% of our genes and had almost no genes that had an padj of <.1.  We refiltered using a sum of the row >10 which will remove genes with a low count across all of our conditions but will leave those that may have a low count in one condition and a high count in another.  
