---
title: "Wine Clustering with GMM vs KMeans"
excerpt: "A scientific exploration of clustering wine samples using Gaussian Mixture Models and KMeans — complete with dimensionality reduction, cluster validation metrics, interpretability tools, and real-world business relevance."
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

## Project Overview

How can we discover natural groupings in complex data when no labels are provided?

This project tackles that challenge by applying unsupervised learning to the **UCI Wine Dataset** — clustering wine samples based solely on their **chemical composition**. The objective was to compare two widely used algorithms:

- **KMeans** – a fast, hard-clustering algorithm
- **Gaussian Mixture Models (GMM)** – a probabilistic model with soft-clustering and interpretability advantages

By simulating real-world exploration scenarios where ground truth is unknown, this project reflects the decision-making process that many data professionals face in business, science, and technology domains.

---

## Methodology

To ensure scientific rigor and interpretability, the project followed this structured approach:

### 1. Dataset & Preprocessing
- **Data Source**: UCI Wine Dataset, accessed via `sklearn.datasets.load_wine()`
- **Features**: 13 numerical descriptors (e.g., alcohol content, flavonoids, color intensity)
- **Standardization**: Applied `StandardScaler` to normalize scales

### 2. Cluster Number Selection
- **Elbow Method**: Based on inertia for KMeans  
- **Silhouette Score**: Internal validation of cluster cohesion  
- **AIC & BIC**: For GMM complexity control

### 3. Modeling
- **KMeans**: Partition-based algorithm with hard assignments  
- **GMM**: Soft probabilistic model using maximum likelihood  
- **DBSCAN**: Added as a density-based contrast

### 4. Dimensionality Reduction
- **PCA**: For initial 2D projection and visual clustering  
- **t-SNE**: For non-linear manifold inspection and deeper visual insights

### 5. Evaluation Metrics
- **ARI (Adjusted Rand Index)**: Measures alignment with true cultivars  
- **Silhouette Score**: Cluster separation and compactness  
- **DBI (Davies-Bouldin Index)**: Penalizes overlapping or scattered clusters  
- **Entropy Analysis**: Quantifies uncertainty in GMM assignments  
- **Confusion Matrices**: For intuitive understanding of clustering precision

---

## Results Summary

| Model   | ARI   | Silhouette | DBI    | AIC     | BIC     |
|---------|-------|------------|--------|---------|---------|
| GMM     | 0.880 | 0.2844     | 1.3938 | 4807.2  | 5806.3  |
| KMeans  | 0.898 | 0.2849     | 1.3892 | —       | —       |

- **KMeans** showed slightly better ARI and DBI scores, indicating tighter and more accurate clustering in this dataset.
- **GMM** excelled in *interpretability*, providing probability surfaces, confidence heatmaps, and entropy histograms that reveal uncertainty — an essential feature for decision support in domains like medicine and finance.

---

## Key Visual Insights

- **PCA Scatter Plots** comparing true vs. predicted clusters
- **GMM Decision Boundaries** revealing soft transition zones
- **Confidence Heatmaps** highlighting certainty of assignments
- **t-SNE Plots** displaying complex, nonlinear relationships
- **Entropy Distributions** for uncertainty quantification
- **Confusion Matrices** showing where models succeed (or fail)

These tools bridge the gap between technical performance and stakeholder interpretability — ensuring the results aren’t just statistically sound, but also *communicable*.

---

## Real-World Applications

This project’s techniques are widely applicable in many fields:

- **Food & Beverage**: Grouping products by sensory or chemical profiles  
- **Bioinformatics**: Discovering cell types or gene expression clusters  
- **Retail & E-commerce**: Customer segmentation for personalization  
- **Healthcare**: Clustering patients by diagnostic or treatment profiles  
- **Cybersecurity**: Detecting anomalous user behavior without prior labels

---

## Explore the Code and Notebook

- 🔗 [GitHub Repository](https://github.com/victoropp/wine-clustering-gmm-kmeans)  
- 🔗 [Kaggle Notebook](https://www.kaggle.com/code/victoropp/clustering-gmm-vs-kmeans-on-wine-dataset)

---

## About the Author

**Victor Collins Oppon** is an MSc Data Science candidate at Middlesex University, UK. With over 15 years of experience in finance and business strategy, he brings a multidisciplinary lens to machine learning — blending rigorous statistical thinking, real-world applicability, and a deep commitment to interpretability and communication.

---

> This project is part of Victor’s public data science portfolio — built to demonstrate end-to-end machine learning expertise, domain relevance, and an ability to translate insights into action.

