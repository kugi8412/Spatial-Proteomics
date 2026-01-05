# Spatial-Proteomics

## Neighborhood Representation

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kugi8412/Spatial-Proteomics/blob/main/Cellcharter_Project.ipynb)

Using the `Cellcharter` library to calculate cell neighbourhood representations and then analyse them.
For a comprehensive understanding of the command, [read](https://github.com/kugi8412/Spatial-Proteomics/blob/main/Description.pdf).

The task consists of the following step:
* PCA on cells marker expressions, which explain 95% of markers variance.
* Cellcharter neighbor aggregation.
* Cluster selection in the same manner as for mean marker.
* PCA, celltype abundance and mean marker analysis in the same manner as for mean marker and cell type histogram representations.
* Clusterings out of mean marker, cell type histogram and cellcharter-based ones.

The use of different methods shows that a key parameter is the range of values of the clusters searched for in order to select the most stable one. In addition, the analyses can be extended to include hierarchical clustering, where we first extract the main clusters and then within each of these we perform a further, more detailed clustering.

## [Other approaches](https://github.com/kugi8412/Spatial-Proteomics/blob/main/SCVI_and_BertCharter/Additional_assignment.pdf) 🆚 PCA

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kugi8412/Spatial-Proteomics/blob/main/SCVI_and_BertCharter/SCVI%26BERT-Charter.ipynb)

### SCVI
The single-cell Variational Inference (scVI) algorithm is a deep probabilistic model specifically designed for analyzing single-cell RNA sequencing technology (scRNA-seq) data or similar gene expression/marker data at the single-cell level, which often have specific problems such as high sparsity. The scVI generative model assumes that the observed gene expression in each cell is the result of a complex process that can be modeled. The main idea is to reduce the high-dimensional data to a low-dimensional hidden space (e.g., corresponding to the number of markers) This hidden space is supposed to capture the important biological variability between cells, while dealing with technical artifacts. The algorithm uses deep learning and variational inference techniques to learn model parameters and estimate the hidden representation (embeddings) for each cell.

### BERT-Charter
BertCharter is a model based on the Transformer Encoder architecture. Inspired by the BERT (Bidirectional Encoder Representations from Transformers) model, it has been adapted to analyse local cellular microenvironments in spatial data. The standard BERT model was originally developed for natural language processing (NLP), where it learns contextual representations of words in sentences. In BertCharter, this concept is applied to the analysis of biological data as follows:
* Rather than a sequence of words, a _sentence_ is a sequence of cells in the neighbourhood of a central cell.
* A _word_ is a cell with its expressed markers.
* _Word embedding_ represents the cell and its position in the neighbourhood.

## Resources 🔗
[Cellcharter package](https://github.com/CSOgroup/cellcharter)

[Spatial clustering tutorial](https://cellcharter.readthedocs.io/en/stable/notebooks/cosmx_human_nsclc.html)

[scBERT](https://www.biorxiv.org/content/10.1101/2021.12.05.471261v1)

[A useful resource about Spatial Data Mining](https://zk.gik.pw.edu.pl/zasoby/publikacje/SDM_monografia.pdf)
