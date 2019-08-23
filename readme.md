# Initial thoughts:
* see:
Development of an Analysis Pipeline Characterizing Multiple Hypervariable Regions of 16S rRNA Using Mock Samples 
Barb JJ, Oler AJ, Kim HS, Chalmers N, Wallen GR, et al. (2016) Development of an Analysis Pipeline Characterizing Multiple Hypervariable Regions of 16S rRNA Using Mock Samples. PLOS ONE 11(2): e0148047. https://doi.org/10.1371/journal.pone.0148047

* Oveerview:
    * Preprocessing
        * Quality & length filtering - fastq filter script from USEARCH suite of tools (fastq_filter)
            * Removed if less than 200 bp and had more than 1 total expected number of errors for all bases in the read (would need to change for my study since reads are shorter than that).
        * Adding read blocks to order to mimic non-demultiplexed data for downstream analysis
            * Read IDs edited and formated to match downstream procesing pipeline using UPARSE and QIIME so that a read ID contained "Ex##;barcodelabel = [sample name];" where '##' is a number in numerical order and 'sample name' is the sample 
        * Concatenating reads into one file
            * So that one fasta file contains reads from all samples in the study to mimic non-demuliplexed data.
    * Separating reads into different variable regions
        * Aligned the full set of reads with the Mothur script align.seqs
        * Don't need to do this because mine are already separated by region?

* Necessary resources:
    * USEARCH?
    * QIIME2 - installed
