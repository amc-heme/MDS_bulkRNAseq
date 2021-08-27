# MDS_rstudio
an Rstudio document to process all the MDS_bulk_RNAseq data

This document is looking at the analysis of the original 9 samples of the MDS bulk RNAseq data from Brett Stevens.  This data was collected on 07/21/15, 09/14/14 
and 12/03/14.  There are 3 patients that each have 3 samples: Bulk, CD123-, CD123+.  These samples were prepared with the Illumina Truseq protoocol.  
They are unstranded and SE100 bp.  The data were analyzed with FASTP, trimmed with cutadapt using the Truseq adapter and aligned with Salmon v1.3.0 and STAR 2.7.9a using the human gencode V38 genome.
