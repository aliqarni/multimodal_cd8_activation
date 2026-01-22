# 🧬 Melanoma Multi-Omics (CITE-seq)

This repository contains a multimodal single-cell analysis pipeline using CITE-seq data from melanoma patients treated with immune checkpoint inhibitors.

Dataset: *GSE289084*

---

## 📌 Data Modalities

- *scRNA-seq* → Gene expression (transcriptome)  
- *ADT (CITE-seq)* → Surface protein expression (proteome)  

Both measurements are from the *same single cells*, enabling direct RNA–protein integration.

---

## 🧠 Biological Definitions

| Cell State        | Meaning |
|------------------|--------|
| *HLA-DR⁺ CD8⁺* | Activated CD8⁺ T cells |
| *HLA-DR⁻ CD8⁺* | Resting CD8⁺ T cells |
| *CD8⁺*         | Cytotoxic T lymphocytes |
| *HLA-DR*       | Marker of immune activation |

Activation is defined using the *top 20% of HLA-DR protein expression*.

---

## 🔬 Methods

- Loaded and aligned:
  - RNA count matrix  
  - ADT protein matrix  
  - Cell-level metadata  

- Defined immune states:
  - *HLA-DR⁺ CD8⁺* (activated)
  - *HLA-DR⁻ CD8⁺* (resting)

- Compared:
  - RNA expression between activation states  
  - Protein expression between activation states  
  - Patient-wise immune heterogeneity  

- Computed:
  - log2 fold-changes  
  - Activation specificity scores  
  - RNA–protein correlations  

- Built:
  - Biomarker scatter plots  
  - RNA vs ADT concordance plots  
  - Multimodal embeddings using *TotalVI*

---

## 🧬 Candidate Biomarkers

Examples identified during analysis:

- *NKG7*
- *GNLY*
- *GZMB*
- *PRF1*
- *HLA-DRA / HLA-DRB1*
- *CD8A / CD8B*
- *TOX*
- *PTPRC (CD45)*

These genes show activation-specific behavior in *HLA-DR⁺ CD8⁺* cells.

---

## 🧠 Multimodal Learning

Used *TotalVI (scvi-tools)* to:

- Jointly model RNA + ADT  
- Learn a shared latent space  
- Visualize immune activation patterns  
- Validate RNA–protein consistency  

---

## 🛠 Tools Used

- Python  
- Pandas, NumPy  
- Scanpy  
- scvi-tools (TotalVI)  
- Matplotlib / Seaborn  
- Bash (for large matrix slicing)
