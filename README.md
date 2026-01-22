🧬 Melanoma Multi-Omics: Multimodal CITE-seq Analysis of Immune Activation

This repository contains a complete multimodal, multi-omics single-cell analysis pipeline using CITE-seq data to study immune activation in melanoma patients treated with immune checkpoint inhibitors.
We integrate:
scRNA-seq (RNA) → transcriptome
ADT (CITE-seq proteins) → surface proteome
to identify and characterize activated CD8⁺ T cells (HLA-DR⁺ CD8⁺), study patient heterogeneity, and discover RNA–protein biomarkers of immune response.
Dataset: GSE289084 (NCBI GEO)

🎯 Project Goals
Define immune activation states using protein markers (HLA-DR, CD8)
Compare:
HLA-DR⁺ CD8⁺ (activated CD8 T cells)
HLA-DR⁻ CD8⁺ (resting CD8 T cells)
Quantify:
RNA changes associated with activation
Patient-wise heterogeneity
Discover:
Activation-specific RNA biomarkers
RNA–protein concordant signatures
Learn:
Joint RNA–protein latent representations using TotalVI

🔬 Biological Concept
State
Meaning
HLA-DR⁺ CD8⁺
Activated cytotoxic T cells
HLA-DR⁻ CD8⁺
Resting / baseline CD8 T cells
Protein defines cell identity.
RNA explains cell function.
This makes the project:
Multi-omics → transcriptome + proteome
Multimodal → RNA + protein as separate data modalities

🧠 Computational Methods
CITE-seq preprocessing (RNA + ADT matrices)
Cell metadata reconstruction from barcodes
HLA-DR thresholding (top 20% activation definition)
CD8 stratification
Differential expression using log2 fold-change
Activation-specificity scoring
RNA–protein concordance analysis
Bash-based RNA matrix subsetting for Colab efficiency
Multimodal generative modeling with TotalVI
Joint RNA–protein latent space visualization

📊 Core Analyses Performed
Protein-based immune activation stratification
RNA signatures of activated CD8⁺ T cells
Per-patient immune activation scoring
RNA vs ADT correlation (e.g., HLA-DR RNA vs protein)
Multimodal embedding showing:
Activated cells distributed across latent space
Resting cells forming compact clusters
Identification of candidate biomarkers such as:
NKG7, GNLY, PRF1, GZMB, TOX, CD8A/B, HLA-DRA/B, FCGR3A, SELL, PTPRC

🧪 Example Biological Signals
Activated CD8⁺ transcriptome:
Cytotoxic genes (GNLY, PRF1, GZMB)
Immune exhaustion / regulation markers (TOX)
Antigen presentation (HLA-DRA/B)
RNA–Protein Concordance:
Strong correlation between HLA-DR protein and HLA-DRA/B RNA
Patient-wise immune activation heterogeneity across therapy

🛠️ Tools & Technologies
Python, Pandas, NumPy
Scanpy, Anndata
scvi-tools (TotalVI)
Matplotlib / Seaborn
Bash (zgrep for RNA slicing)
