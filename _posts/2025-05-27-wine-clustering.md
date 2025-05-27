---
title: "Wine Clustering with GMM vs KMeans"
excerpt: "A scientific clustering project comparing Gaussian Mixture Models and KMeans using PCA, t-SNE, DBSCAN, and full metric evaluation on the UCI Wine dataset."
layout: single
date: 2025-05-27
author_profile: true
read_time: true
classes: wide
tags: [clustering, machine-learning, unsupervised-learning, gmm, kmeans, pca, tsne, portfolio]
header:
  overlay_image: /assets/images/wine-banner.png
  overlay_filter: 0.2
  caption: "Scientific clustering with Python and scikit-learn"
  actions:
    - label: "View on GitHub"
      url: "https://github.com/victoropp/wine-clustering-gmm-kmeans"
    - label: "View on Kaggle"
      url: "https://www.kaggle.com/code/victoropp/clustering-gmm-vs-kmeans-on-wine-dataset"
---

## Overview

In this project, I applied unsupervised machine learning techniques to cluster wine samples using only their chemical attributes — no labels or cultivars provided. This mirrors how real-world analysts must explore data without knowing the true structure beforehand.

The project compared **Gaussian Mixture Models (GMM)** with **KMeans**, using:

- Cluster number selection via Elbow, Silhouette, AIC, and BIC
- Dimensionality reduction using PCA and t-SNE
- Evaluation with ARI, DBI, Silhouette Score
- Interpretability tools like entropy histograms and GMM confidence heatmaps

---

## Methodology

- **Dataset**: UCI Wine Dataset (via `sklearn.datasets.load_wine()`)
- **Features**: 13 numerical chemical components
- **Clusters**: Auto-selected via multiple metrics
- **Models**: GMM, KMeans, DBSCAN
- **Visualizations**: PCA, t-SNE, decision boundaries, entropy, confusion matrices

---

## Results Summary

| Model   | ARI   | Silhouette | DBI   | AIC     | BIC     |
|---------|-------|------------|-------|---------|---------|
| GMM     | 0.880 | 0.2844     | 1.3938| 4807.2  | 5806.3  |
| KMeans  | 0.898 | 0.2849     | 1.3892| —       | —       |

GMM provided more interpretability via soft-clustering and probability heatmaps, while KMeans offered slightly better ARI and DBI.

---

## Real-World Applications

- **Food science**: Wine profiling
- **Bioinformatics**: Genetic clustering
- **Retail analytics**: Customer segmentation
- **Healthcare**: Diagnostic clustering
- **Cybersecurity**: Unsupervised anomaly detection

---

## Links

-  [GitHub Repository](https://github.com/victoropp/wine-clustering-gmm-kmeans)
-  [Kaggle Notebook](https://www.kaggle.com/code/victoropp/clustering-gmm-vs-kmeans-on-wine-dataset)

---

## About the Author

Victor Collins Oppon is an MSc Data Science candidate at Middlesex University (UK), transitioning from a 15-year career in finance and business strategy. His work emphasizes statistical integrity, real-world relevance, and clear communication of machine learning solutions.
