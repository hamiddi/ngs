# Bioinformatics: A Practical Guide to Next Generation Sequencing Data Analysis

This repository contains curated datasets, example scripts, and supplementary resources to accompany the textbook **Bioinformatics: A Practical Guide to Next Generation Sequencing Data Analysis** authored by Dr. Hamid D. Ismail.

The book provides a comprehensive guide to the theoretical foundations and practical implementation of NGS data analysis using modern bioinformatics techniques and tools. This repository aims to help readers follow hands-on examples and execute pipelines for learning and research purposes.

## 📘 Book Chapters Overview

Below is a summary of the chapters covered in the book and the supplementary materials provided in this repository:

### Chapter 1: Sequencing and Read Quality

- Overview of DNA/RNA structure and sequencing history  
- Introduction to Sanger and Next-Generation Sequencing (NGS)  
- Quality control of sequencing reads (e.g., FastQC, Trimmomatic)  
- Sample datasets: `data/reads/`  
- Scripts: `scripts/quality_control/`  

### Chapter 2: Sequence Read Alignment

- Concept of reference genomes and alignment  
- Read mappers: `BWA`, `Bowtie2`, `STAR`  
- Indexing reference genomes using Samtools  
- Outputs: SAM/BAM formats  
- Example dataset: `data/alignment/`  
- Scripts: `scripts/alignment/`  

### Chapter 3: De Novo Genome Assembly

- Assembly strategies (greedy, overlap-layout-consensus, de Bruijn graphs)  
- Tools: `SPAdes`, `ABySS`, `Velvet`  
- Use of paired-end reads for long contigs  
- Sample datasets: `data/assembly/`  
- Scripts: `scripts/assembly/`  

### Chapter 4: Variant Discovery

- Types of variants: SNVs, InDels, SVs  
- VCF file format and structure  
- Variant calling pipelines: `bcftools`, `GATK`  
- Variant annotation: `SnpEff`, `ANNOVAR`  
- Sample datasets: `data/variants/`  
- Scripts: `scripts/variant_calling/`  

### Chapter 5: RNA-Seq Data Analysis

- Transcriptomics and gene expression profiling  
- Differential gene expression analysis  
- Tools: `featureCounts`, `DESeq2`, `edgeR`  
- Applications: isoform detection, eQTL, ASE  
- Datasets: `data/rnaseq/`  
- Scripts: `scripts/rnaseq/`  

### Chapter 6: ChIP-Seq Analysis

- Chromatin structure and epigenetic modifications  
- Peak calling and motif analysis  
- Tools: `MACS2`, `HOMER`, `ChIPseeker`  
- Control sample normalization  
- Datasets: `data/chipseq/`  
- Scripts: `scripts/chipseq/`  

### Chapter 7: Targeted Gene Metagenomics

- Amplicon-based (16S rRNA) microbiome profiling  
- OTU clustering and ASV inference  
- Tools: `QIIME2`, `DADA2`, `USEARCH`, `CD-HIT`  
- Diversity metrics and taxonomic assignment  
- Datasets: `data/metagenomics_targeted/`  
- Scripts: `scripts/metagenomics_targeted/`  

### Chapter 8: Shotgun Metagenomic Analysis

- Assembly-based and assembly-free approaches  
- Taxonomic binning: `MetaBAT2`, `MaxBin`  
- Functional profiling: `HUMAnN`, `Kraken2`, `Kaiju`  
- MAG (Metagenome-Assembled Genomes) generation  
- Datasets: `data/metagenomics_shotgun/`  
- Scripts: `scripts/metagenomics_shotgun/`  

## 🧪 Software Requirements

Most examples use standard command-line tools and open-source software. Suggested environments:

- Linux (Ubuntu or CentOS)  
- Python ≥ 3.8  
- R ≥ 4.0  
- Conda/Miniconda  
- Tools: FastQC, Trimmomatic, STAR, Samtools, GATK, DESeq2, MACS2, QIIME2, etc.  

The conda environment YAML file `environment.yml` is provided.

## 📖 Citation

Please cite the textbook when using this repository:

> Ismail, H.D. (2023). *Bioinformatics: A Practical Guide to Next Generation Sequencing Data Analysis* (1st ed.). Chapman and Hall/CRC. https://doi.org/10.1201/9781003355205

---

If you find this repository useful, please ⭐ star it and share your feedback or issues via GitHub.
