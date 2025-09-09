# 🧬 SCDCC

**Single-Cell Data Clustering & Classification (SCDCC)**  

This repository contains Jupyter notebooks for analyzing **single-cell transcriptomics datasets**.  
It demonstrates end-to-end workflows including preprocessing, dimensionality reduction, clustering, and visualization applied across multiple datasets.  

---

## 📂 Repository Contents

- `Mouse_Bladder.ipynb` – Analysis of mouse bladder dataset  
- `Worm_Neuron.ipynb` – Analysis of worm neuron dataset  
- `Zeisel mouse brain.ipynb` – Analysis of mouse brain (cortex + CA1) dataset  
- `pbmc-10k.ipynb` – Analysis of PBMC-10k dataset  
- `Data Sets/` – Directory for datasets used in the experiments  
- `requirements.txt` – Python dependencies  

---

## 🏗️ Project Architecture

The workflow across all notebooks generally follows these steps:

1. **Data Loading** – Import scRNA-seq datasets from local files or public repositories  
2. **Preprocessing & QC** – Filtering of low-quality cells, normalization, and feature selection  
3. **Dimensionality Reduction** – PCA, t-SNE, or UMAP for low-dimensional embeddings  
4. **Clustering** – Identify cell populations using unsupervised clustering  
5. **Visualization** – Generate scatter plots, heatmaps, and expression profiles  
6. **Interpretation** – Annotate clusters with potential biological cell types  

---

## 🔬 Model Architecture

This project applies both **unsupervised clustering** and **supervised classification** techniques for single-cell data analysis:  

- **Preprocessing Layer**  
  - Cell filtering, gene filtering, log-normalization, scaling  
  - Selection of highly variable genes  

- **Dimensionality Reduction**  
  - **PCA** for linear reduction  
  - **t-SNE / UMAP** for non-linear embeddings  

- **Clustering Algorithms**  
  - **K-Means clustering**  
  - **Graph-based clustering** (Louvain / Leiden if using Scanpy)  

- **Classification Models (optional, supervised)**  
  - Logistic Regression  
  - Random Forests / Decision Trees  
  - Other ML classifiers for labeled datasets  

- **Visualization & Interpretation**  
  - 2D cluster maps (UMAP/t-SNE)  
  - Heatmaps of gene expression  
  - Marker gene analysis for cluster annotation  

---

## 📊 Datasets

This project uses several **publicly available single-cell RNA-seq datasets**:

- **Mouse Bladder** – Bladder cell transcriptomic profiles  
  *Source: [NCBI GEO](https://www.ncbi.nlm.nih.gov/geo/)*  

- **Worm Neurons (C. elegans)** – Single-cell neuronal dataset  
  *Source: [WormBase](https://wormbase.org/)*  

- **Zeisel Mouse Brain (Cortex + CA1)** – Annotated neurons from mouse brain regions  
  *Source: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE60361
 )*  

- **PBMC-10k (Human)** – Peripheral blood mononuclear cells (~10,000 cells)  
  *Source: [10x Genomics](https://www.10xgenomics.com/resources/datasets)*  

👉 Large datasets may need to be downloaded separately and placed inside the `Data Sets/` folder.  

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Rachit-Singhal-01/Scdcc.git
cd Scdcc

