# McDonald's Dataset Analysis and Clustering

This repository contains Python code for analyzing the McDonald's dataset using clustering, PCA, and Gaussian Mixture Models. The project covers data preprocessing, dimensionality reduction, segmentation, and visualization.

## Table of Contents

- [Introduction](#introduction)
- [Preprocessing](#preprocessing)
- [PCA Analysis](#pca-analysis)
- [K-Means Clustering](#k-means-clustering)
- [Global and Segment Stability](#global-and-segment-stability)
- [Gaussian Mixture Models](#gaussian-mixture-models)
- [Hierarchical Clustering](#hierarchical-clustering)
- [Segment Profiling](#segment-profiling)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [License](#license)

---

## Introduction

This project applies various unsupervised machine learning techniques to explore and segment data from a McDonald's survey. Techniques include:
- Principal Component Analysis (PCA)
- K-Means Clustering
- Gaussian Mixture Models (GMM)
- Hierarchical Clustering

Visualizations and metrics such as Adjusted Rand Index (ARI) and Within-Cluster Sum of Squares (WCSS) are used to evaluate stability and interpret the clusters.

---

## Preprocessing

### Steps:
1. **Binary Encoding:** Converted categorical responses (e.g., "Yes"/"No") into binary variables.
2. **Scaling:** Standardized features using `StandardScaler` for clustering and PCA.
3. **Label Encoding:** Categorical columns like `Gender` and `VisitFrequency` were encoded numerically.

### Key Operations:
- Converted "Like" ratings to a numeric scale.
- Checked data types and ensured all features were numeric.

---

## PCA Analysis

- Performed PCA to understand the variance explained by each component.
- Plotted the first two principal components for visualization.
- Explored the loadings of each feature on the principal components.

### Key Outputs:
- Explained Variance Ratio
- Cumulative Variance
- PCA Projection Plot
- PCA Loadings Plot

---

## K-Means Clustering

- Determined optimal number of clusters using the Elbow Method.
- Analyzed clustering results for segment profiling.

### Scree Plot:
- Showcased the Within-Cluster Sum of Squares (WCSS) for clusters ranging from 2 to 8.

---

## Global and Segment Stability

- Used bootstrap resampling to calculate ARI scores across different cluster solutions.
- Plotted Segment-Level Stability Across Solutions (SLSA) and Segment-Level Stability Within Solutions (SLSW).

### Tools:
- `sklearn.metrics.adjusted_rand_score`
- `matplotlib` for stability plots.

---

## Gaussian Mixture Models

- Fitted Gaussian Mixture Models to explore data segments as probabilistic distributions.
- Evaluated AIC and BIC to determine the number of components.
- Compared GMM clusters with K-Means clusters.

---

## Hierarchical Clustering

- Performed hierarchical clustering using Ward's method.
- Created a dendrogram to visualize attribute clustering.

---

## Segment Profiling

- Grouped data by clusters to explore feature distributions within each segment.
- Visualized feature distributions using:
  - Boxplots for numerical variables.
  - Count plots for categorical variables.

---

## Dependencies

Ensure the following Python libraries are installed:

```bash
numpy
pandas
matplotlib
seaborn
scikit-learn
