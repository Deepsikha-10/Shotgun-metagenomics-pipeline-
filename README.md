# Shotgun-metagenomics-pipeline-
A shotgun metagenomics pipeline for analysis of paired end human microbiome sample (SRR6664507) from raw-reads to taxonomic profiling.
This pipeline implements a complete workflow for shotgun metagenomic analysis, including:

- **Quality Control**: Raw read QC, adapter trimming, and host DNA removal
- **Host Removal**: Only non-host reads are kept in this step.
- **Assembly Construction**: Reconstructed contigs from non-host reads.
- **Taxonomic Profiling**: Assign taxonomic labels to assembled contigs and estimate relative abundances of taxa.
- **Functional Annotation**: Predict genes and annotate their functions in assembled contigs.
- **Visualization**: Interactive plots and summary statistics.

## Pipeline Workflow

1. **Preprocessing**
   - FastQC quality assessment
   - Adapter and quality trimming (Trimmomatic)
   - Human host DNA removal (Bowtie2/BWA)

2. **Taxonomic Profiling**
   - MetaPhlAn4/Kraken2 for species identification
   - Bracken for abundance estimation
   - Krona plots for visualization

3. **Functional Profiling**
   - Predict genes and assign functional annotations to assembled contigs using Prokka,eggNOG-mapper.
   - KEGG/COG pathway mapping
   - Antibiotic resistance gene detection (optional)
     
## Output
The pipeline generates:
- Quality control reports
- Taxonomic abundance tables 
- Functional profile matrices (gene families, pathways)
- Interactive visualizations

## Use Cases

- Human gut microbiome studies
- Oral/skin microbiome analysis
- Disease vs. healthy comparisons
- Multi-omics integration

  
