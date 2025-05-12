# Spatial-Proteomics

## Neighborhood Representation
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

### SCVI

### BERT-Charter

## Resources 🔗
[Cellcharter package](https://github.com/CSOgroup/cellcharter)

[Spatial clustering tutorial](https://cellcharter.readthedocs.io/en/stable/notebooks/cosmx_human_nsclc.html)
