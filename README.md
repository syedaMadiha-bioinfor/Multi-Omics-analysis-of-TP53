# Multi-Omics-Analysis-of-TP53
Objective : Analyze TP53 mutations using NGS data, integrate RNA-Seq gene expression  data, and apply AI/ML models for insights

## step 1: Genomics and data retrieval
Tools: NCBI, Ensembl, UCSC Genome Browser, Galaxy 
1. Retrieve Genomic Data:  
o Download TP53 gene sequence from NCBI Gene Database. 
o Extract mutations from dbSNP or COSMIC Mutation Database. 
2. Obtain Cancer Datasets:  
o Download TP53 mutation datasets from TCGA (via UCSC Xena 
or GDC Data Portal). 
o RNA-Seq data for cancer types (e.g., Lung, Breast, Colon, etc.)

## step 2: NGS Variant Calling Pipeline
A comprehensive, modular pipeline for calling variants from next-generation sequencing (NGS) data. This pipeline streamlines the analysis from raw sequencing reads to annotated variant calls, making it easier to integrate into your bioinformatics workflows

### Overview
The NGS Variant Calling Pipeline automates the key steps in variant analysis, including:

+ Quality Control: Assessing raw read quality (e.g., using FastQC).
+ Read Alignment: Mapping reads to a reference genome (e.g., using BWA or Bowtie).
+ Post-processing: Sorting, indexing, and marking duplicates (e.g., with Samtools and Picard).
+ Variant Calling: Identifying single nucleotide variants and indels (e.g., using GATK or FreeBayes).
+ Annotation: Adding biological context to identified variants (e.g., using GATK).
This pipeline is designed with modularity and reproducibility in mind, allowing you to easily customize and extend its functionality.
### Features
- Modular Design: Swap out or add tools based on your needs.
- Automation: End-to-end processing from raw data to variant reports.
- Scalability: Suitable for both small datasets and large-scale studies.
- Reproducibility: Configuration files and version control ensure that analyses can be replicated.

### Requirements
Operating System: Linux-based systems (tested on Ubuntu)
Programming Language: Python 3.6 or higher
Tools:
- [Git](https://git-scm.com/)
- [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
- [Samtools](https://www.htslib.org/)
- [Picard](https://broadinstitute.github.io/picard/)
- [GATK](https://gatk.broadinstitute.org/hc/en-us) or [FreeBayes](https://github.com/freebayes/freebayes)



## step 3:  RNA-Seq Analysis Pipeline
A comprehensive, modular pipeline for RNA sequencing (RNA-Seq) analysis. This pipeline streamlines the process from raw sequencing reads to differential gene expression analysis, making it easier to integrate into your bioinformatics workflows.
	
### Overview
The RNA-Seq Analysis Pipeline automates the key steps in gene expression analysis, including:

- Data Acquisition: Downloading RNA-Seq data from the Sequence Read Archive (SRA), along with reference genome and annotation (GTF) files.
- Pre-processing: Converting SRA files to FASTQ format, assessing read quality using FastQC and MultiQC, and trimming adapters/low-quality bases with Trimmomatic.
- Read Alignment: Mapping reads to a reference genome using HISAT2.
- Post-alignment Processing: Sorting and indexing BAM files using Samtools.
- Quantification: Counting reads per gene using featureCounts.
- Differential Expression Analysis: Identifying differentially expressed genes using DESeq2 in R, along with visualizations such as volcano plots, MA plots, PCA plots, and heatmaps.
This pipeline is designed with modularity and reproducibility in mind, allowing you to easily customize and extend its functionality.

### Features
- Modular Design: Easily swap out tools or add new ones based on your requirements.
- Automation: End-to-end processing from raw RNA-Seq reads to gene expression results.
- Scalability: Suitable for both small experiments and large-scale transcriptomic studies.
- Reproducibility: Configuration files and version control ensure that analyses can be replicated.

### Requirements
* Operating System: Linux-based systems (tested on Ubuntu)
* Programming Language: Bash, R (for differential expression analysis)
* Tools:
- [Git](https://git-scm.com/)
- [SRA Toolkit](https://github.com/ncbi/sra-tools/wiki/01.-Downloading-SRA-Toolkit)
- [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
- [MultiQC](https://seqera.io/multiqc/)
- [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)
- [HISAT2](https://daehwankimlab.github.io/hisat2/)
- [Samtools](https://www.htslib.org/)
- [featureCounts](https://bioinf.wehi.edu.au/featureCounts/)
- [R](https://www.r-project.org/) with [DESeq2](https://bioconductor.org/packages/release/bioc/html/DESeq2.html)

						             
## step 4: AI & Machine Learning for Mutation Classification
1. Prepare Data:  
o Combine mutation features + gene expression profiles. 
o Label samples as TP53-mutant or wild-type. 
2. Build ML Models:  
o Use Google AutoML Tables for automated feature selection and 
model training. 
o Use Orange3 for interactive ML analysis (Decision Trees, Random 
Forest, SVM). 
o Train classification models in Google Colab using Scikit-learn 
(Random Forest, SVM, XGBoost). 
3. Evaluate Model Performance:  
o Compute accuracy, F1-score, and AUC-ROC.

Tools: Google AutoML Tables, Orange3, Google Colab (ML tools)

## Step 5: Multi-Omics Integration & Pathway Analysis 
1. Merge Genomic & Transcriptomic Data:  
o Integrate variant data + RNA-Seq gene expression. 
2. Functional Enrichment Analysis:  
o Use KEGG/Reactome to identify impacted pathways. 
o Analyze metabolic impact using MetaboAnalyst. 
3. Network Analysis:  
o Construct interaction networks of TP53-associated genes in 
Reactome.

Tools: Galaxy, MetaboAnalyst, KEGG, Reactome

Final Project Deliverables :page_facing_up:
1.Mutation & Expression Data Report 
2.Machine Learning Model Performance Summary 
3.Multi-Omics Pathway Analysis Report 
4.Visualizations (PCA, Heatmaps, Volcano Plots, ROC Curves)
