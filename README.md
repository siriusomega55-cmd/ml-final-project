# Final Project, Option 3: How much structure can you find without the labels?

**Author:** CHRYSOSTOMI ATHINA SKOUDAROPOULOU
**Course:** Machine Learning with Python
**Date:** 4 OCTOBER 2026

## Introduction

In this project I explored the Seeds data set, which contains 210 wheat kernels described by seven geometric measurements. The variety labels were set aside at the start and used only at the very end as an external check.

The central question was: **how much of the real variety structure can be recovered using clustering alone?**

I followed the workflow from Module 4:

1. Scaled the seven features with StandardScaler.
2. Reduced them to two dimensions with PCA for visualisation.
3. Applied K-Means clustering.
4. Chose the number of clusters using the elbow method and the silhouette score.
5. Validated the result against the true varieties using a cross-tabulation and a purity score.

## Results summary

- **Chosen k:** 3
- **Purity score:** 0.919
- **Explained variance (2 PCA components):** 88.9%
- **Main finding:** the three clusters matched the three real varieties closely, with only a small number of kernels crossing between clusters.

## Files

- `Final_Project_Option3_Seeds_Clustering.ipynb` — the completed notebook.

## Reflection

The clustering worked well on this data set: the purity score of 0.919 shows that the clusters lined up closely with the real varieties. The elbow method and the silhouette score mostly agreed, which made the choice of k = 3 easier. The main difficulty was remembering that clustering always returns groups, whether or not they are real, so the purity score and the choice of k must be reported together. In the future I would test other clustering algorithms, such as DBSCAN or hierarchical clustering, and check whether they recover the structure more cleanly.
