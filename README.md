# README: Analysis of the CIC-ATXN1L Complex in IFN and ISG Regulation

## Overview
This analysis explores the role of the CIC-ATXN1L complex as a transcriptional repressor in the regulation of interferon (IFN) and interferon-stimulated genes (ISGs). Under homeostatic conditions, CIC-ATXN1L binds to an 8-nucleotide motif near IFN and ISG promoters, preventing their aberrant activation. However, during respiratory viral infections, this repression is lifted due to the degradation of CIC-ATXN1L, mediated by the activation of the Mitogen-activated protein kinase (MAPK) pathway. This mechanism primes host cells for robust antiviral responses through interferon regulatory factors (IRFs) and signal transducer and activator of transcription (STAT) transcription factors.

## Data Description
- The dataset includes gene expression profiles under homeostasis and viral infection conditions.
- RNA sequencing (RNA-seq) data captures transcriptional changes following CIC-ATXN1L depletion.
- Experimental validation includes knockout (KO) and overexpression models in human and murine cell lines.

## Data Source
- Link: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE271898
## Key Findings
1. **CIC-ATXN1L as a Repressor:** CIC-ATXN1L binds directly to IFN and ISG promoters, suppressing their activation in the absence of infection.
2. **MAPK Pathway Activation:** Viral infection induces MAPK signaling (assumed in the dataset), leading to CIC-ATXN1L degradation and subsequent relief of repression.
3. **Conserved Mechanism in Murine Models:** Similar regulatory patterns are observed in murine species, suggesting evolutionary conservation.
4. **Functional Consequences:** Loss of CIC-ATXN1L results in spontaneous IFN and ISG expression, potentially leading to auto-inflammatory responses.

## Methods
- **RNA-seq Analysis:** Determines differential gene expression between control and CIC-ATXN1L-deficient conditions.
- **Functional Assays:** Measures antiviral response strength & impacted pathways following CIC-ATXN1L depletion.

## Usage Instructions
### Prerequisites
- Python (>=3.8) with required bioinformatics libraries (pandas, numpy, seaborn, scipy, etc.)
- R (>=4.0) with DESeq2 and ggplot2 for RNA-seq analysis
- Bioinformatics tools: Bowtie2, MACS2, STAR, featureCounts

### Running the Analysis
1. Clone the repository and navigate to the project directory.
   ```bash
   git clone <repository_url>
   cd CIC-ATXN1L_analysis
   ```
2. Preprocess raw sequencing data.
   ```bash
   bash scripts/preprocessing.sh
   ```
3. Run ChIP-seq and RNA-seq analysis pipelines.
   ```bash
   python scripts/run_chipseq.py
   Rscript scripts/run_rnaseq.R
   ```
4. Generate visualizations.
   ```bash
   python scripts/plot_results.py
   ```
5. Review results in the `output/` directory.

## Contact
For questions or collaboration inquiries, please reach out to **seoyoung at uni.minerva.edu**.

## Citation
If you use this analysis, please cite:
**Issuree, 2025. The Role of CIC-ATXN1L in IFN and ISG Regulation.**

