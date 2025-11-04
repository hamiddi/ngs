# Bioinformatics: A Practical Guide to Next Generation Sequencing Data Analysis

This repository contains curated datasets, example scripts, and supplementary resources to accompany the textbook **Bioinformatics: A Practical Guide to Next Generation Sequencing Data Analysis** authored by Dr. Hamid D. Ismail.

The book provides a comprehensive guide to the theoretical foundations and practical implementation of NGS data analysis using modern bioinformatics techniques and tools. This repository aims to help readers follow hands-on examples and execute pipelines for learning and research purposes.

## 📘 Book Chapters Overview

Below is a summary of the chapters covered in the book and the supplementary materials provided in this repository:

### Chapter 1: Sequencing and Read Quality

- Overview of DNA/RNA structure and sequencing history  
- Introduction to Sanger and Next-Generation Sequencing (NGS)  
- Quality control of sequencing reads (e.g., FastQC, Trimmomatic)  
- Sample datasets: `data/reads/` - Scripts: `scripts/quality_control/`  

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


# 🧬 NGS Data Analysis: Minimum Hardware Requirements

[![Built with Python](https://img.shields.io/badge/Built%20with-Python-blue.svg)](https://www.python.org/)
[![HPC Ready](https://img.shields.io/badge/HPC%20-Optimized-green)](https://en.wikipedia.org/wiki/High-performance_computing)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

This repository provides **guidelines for minimum computational resources** (CPU cores, RAM, and storage) required for major **Next-Generation Sequencing (NGS)** workflows.  
It is intended for researchers, system administrators, and bioinformaticians designing or scaling analysis pipelines on **workstations, HPC clusters, or cloud environments**.

---

## 🧩  Overview

| Workflow | Description |
|-----------|--------------|
| **General NGS Analysis** | Standard preprocessing and alignment (FastQC, Trimmomatic, BWA, Samtools). |
| **Genome Assembly** | De novo assembly using tools like SPAdes, MEGAHIT, or Canu. |
| **Variant Calling** | SNP/Indel detection and annotation (BWA, GATK, DeepVariant). |
| **RNA-Seq** | Transcript quantification and differential expression (STAR, HISAT2, DESeq2). |
| **ChIP-Seq** | Peak calling and motif discovery (Bowtie2, MACS2). |
| **Amplicon Metagenomics** | 16S/18S/ITS pipelines using QIIME2 or DADA2. |
| **Shotgun Metagenomics** | Whole-metagenome assembly, binning, and annotation (MetaSPAdes, Kaiju, HUMAnN3). |

---

## ⚙️ Minimum Hardware Requirements

### **1. General NGS Data Analysis**

| Resource | Minimum | Recommended |
|-----------|----------|-------------|
| **CPU Cores** | 8 | 16–32 |
| **Memory (RAM)** | 16 GB | 32–64 GB |
| **Storage** | 500 GB | 1–2 TB SSD |

---

### **2. Genome Assembly**

| Resource | Minimum | Recommended |
|-----------|----------|-------------|
| **CPU Cores** | 16 | 32–64 |
| **Memory (RAM)** | 64 GB | 128–512 GB |
| **Storage** | 1–5 TB | ≥10 TB |

> 🧠 Assemblers like SPAdes or Canu are **memory-intensive**. SSDs and large swap partitions improve performance.

---

### **3. Variant Calling**

| Resource | Minimum | Recommended |
|-----------|----------|-------------|
| **CPU Cores** | 8 | 16–32 |
| **Memory (RAM)** | 32 GB | 64–128 GB |
| **Storage** | 1 TB | 2–5 TB |

> Pipelines: **BWA → GATK → VEP/ANNOVAR**

---

### **4. RNA-Seq Analysis**

| Resource | Minimum | Recommended |
|-----------|----------|-------------|
| **CPU Cores** | 8 | 16–32 |
| **Memory (RAM)** | 32 GB | 64 GB |
| **Storage** | 500 GB | 1–2 TB |

> For large genomes (e.g., human), **STAR** indexing alone can require ≥30 GB RAM.

---

### **5. ChIP-Seq Analysis**

| Resource | Minimum | Recommended |
|-----------|----------|-------------|
| **CPU Cores** | 8 | 16 |
| **Memory (RAM)** | 16 GB | 32–64 GB |
| **Storage** | 500 GB | 1 TB |
Typical workflow: **FastQC → Bowtie2 → MACS2 → motif discovery**

---

### **6. Amplicon-Based Metagenomics**

| Resource | Minimum | Recommended |
|-----------|----------|-------------|
| **CPU Cores** | 8 | 16 |
| **Memory (RAM)** | 16 GB | 32–64 GB |
| **Storage** | 200 GB | 500 GB–1 TB |

> Pipelines: **QIIME2**, **DADA2**, or **Mothur**

---

### **7. Shotgun Metagenomics**

| Resource | Minimum | Recommended |
|-----------|----------|-------------|
| **CPU Cores** | 16 | 32–64 |
| **Memory (RAM)** | 64 GB | 128–512 GB |
| **Storage** | 2 TB | 5–10 TB |

> Includes **QC → Assembly (MEGAHIT/MetaSPAdes) → Binning (MetaBAT2) → Annotation (Kaiju/HUMAnN3)**  
> Highly storage- and memory-intensive. Use parallel file systems on HPC for optimal throughput.

---

## 🧠 Summary Table

| Workflow | Min Cores | Min RAM | Min Storage |
|-----------|------------|----------|--------------|
| General NGS | 8 | 16 GB | 500 GB |
| Genome Assembly | 16 | 64 GB | 1 TB |
| Variant Calling | 8 | 32 GB | 1 TB |
| RNA-Seq | 8 | 32 GB | 500 GB |
| ChIP-Seq | 8 | 16 GB | 500 GB |
| Amplicon Metagenomics | 8 | 16 GB | 200 GB |
| Shotgun Metagenomics | 16 | 64 GB | 2 TB |

---

## 💻 Recommended System Setup

| Environment | Description |
|--------------|-------------|
| **Workstation** | Suitable for RNA-Seq or small metagenomics; 32 cores, 128 GB RAM, 4 TB SSD. |
| **HPC Node** | 64–128 cores, 512 GB–1 TB RAM, shared 100 TB storage. |
| **Cloud Setup** | AWS EC2 `r6a.8xlarge` or `c6i.8xlarge`, GCP n2-highmem-64, or Azure HB-series. |

---

## 📖 Citation

Please cite the textbook when using this repository:

> Ismail, H.D. (2023). *Bioinformatics: A Practical Guide to Next Generation Sequencing Data Analysis* (1st ed.). Chapman and Hall/CRC. https://doi.org/10.1201/9781003355205

---

If you find this repository useful, please ⭐ star it and share your feedback or issues via GitHub.
