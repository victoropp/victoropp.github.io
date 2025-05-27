---
title: "Spam Detection Using Naive Bayes in MATLAB"
excerpt: "A production-grade implementation of Naive Bayes classification on the UCI Spambase dataset — including kernel tuning, cross-validation, performance metrics, and real-world deployment with MATLAB."
layout: single
date: 2025-05-23
author_profile: true
read_time: true
classes: wide
tags: [classification, machine-learning, matlab, naive-bayes, spam-detection, nlp, automation, portfolio]
header:
  overlay_image: /assets/images/spam-banner.png
  overlay_filter: 0.25
  caption: "Spam classification in MATLAB using probabilistic learning"
  actions:
    - label: "View on GitHub"
      url: "https://github.com/victoropp/naive-bayes-spam-detection"
      - label: "View on Kaggle"
      url: "https://www.kaggle.com/code/victoropp/spam-detection-in-matlab-naive-bayes-classifier/edit"
---

### Introduction

This post is a deep dive into one of my end-to-end machine learning projects — a spam detection system developed using **MATLAB** and trained on the **UCI Spambase** dataset. This project was not just about building a model — it was about applying the complete lifecycle of data science: from data preprocessing and feature selection to hyperparameter tuning, evaluation, and production-level deployment.

As someone transitioning from finance and strategy into data science, I wanted this project to demonstrate more than technical correctness. It had to show clarity, reproducibility, and impact.

---

## Problem Statement

Email spam is not only a nuisance but a real security risk. Identifying spam efficiently and accurately helps reduce phishing, improve productivity, and secure communication pipelines. The challenge was to build a model that can generalize well to unseen email data while being interpretable and deployable in real systems.

---

## Project Pipeline Overview

The entire project was implemented in MATLAB, and the steps followed are outlined below:

### 1. Dataset

- **Source**: UCI Machine Learning Repository  
- **Dataset**: Spambase (4,601 rows, 57 features + label)
- **Label**: 1 = spam, 0 = non-spam

### 2. Preprocessing

- Removed low-variance features to reduce noise
- Dropped highly correlated features to avoid multicollinearity
- Ensured class balance via stratified sampling

### 3. Model Training

- **Classifier**: Naive Bayes using kernel distribution
- **Optimisation**: Tuned kernel type and smoothing width via Bayesian optimisation
- **Validation**: 5-fold cross-validation

### 4. Evaluation

- ROC curve, AUC, Precision, Recall, and F1 Score
- Bootstrap confidence intervals for accuracy (95%)
- Compared against a logistic regression baseline

### 5. Deployment

- Exported final model using `saveLearnerForCoder` to make it deployable in MATLAB production systems or compiled with MATLAB Coder

---

## Key Features and Enhancements

- **Feature Pruning**: Removed non-informative features to reduce overfitting
- **Hyperparameter Tuning**: Automatically optimised `Width` and `Kernel` using `fitcnb()`'s built-in optimiser
- **Confidence Intervals**: Bootstrap resampling to quantify the uncertainty in accuracy
- **Model Comparison**: Benchmarked against logistic regression
- **Deployment-Ready**: Model saved with `saveLearnerForCoder`, ready for embedding in real-time systems

---

## Results Summary

| Metric            | Result        |
|-------------------|---------------|
| Cross-Validated Accuracy | 85.07%      |
| Final 5-Fold CV Accuracy | 84.85%      |
| Test Accuracy     | 85.94%        |
| Precision         | 0.83752       |
| Recall            | 0.79742       |
| F1 Score          | 0.81698       |
| AUC               | 0.91582       |
| 95% CI (Accuracy) | [83.99%, 87.61%] |

These results indicate a well-balanced classifier with strong generalisation capability.

---

## Learnings and Reflections

Working on this project helped me sharpen my skills in:

- Understanding model tuning and validation in practice
- Thinking about real-world deployment from the beginning
- Evaluating performance beyond just accuracy (e.g., confidence intervals, ROC, AUC)
- Writing clean, modular MATLAB code for reproducibility

It also demonstrated how essential feature engineering and tuning are to model performance — a lesson that applies across all machine learning platforms.

---

## Live Project Links

- **GitHub Repository**: [Spam Detection in MATLAB](https://github.com/victoropp/naive-bayes-spam-detection)  
- **Kaggle Notebook**: [Spam Detection Notebook](https://www.kaggle.com/code/victoropp/spam-detection-in-matlab-naive-bayes-classifier)

---

## What’s Next

This is the first in a series of projects I’m developing as part of my journey from finance to data science. Next up, I’ll be exploring:

- NLP techniques using Altair and Python
- Sentiment analysis across London’s Airbnb reviews
- Xero-integrated Power BI dashboards
- Deep learning models using MATLAB and PyTorch

I’ll share these step-by-step, just like this one.

---

### Interested in more?

Feel free to connect on [LinkedIn](https://www.linkedin.com/in/victor-collins-oppon-fcca-mba-bsc-01541019/), or explore more of my projects on [GitHub](https://github.com/victoropp) and [Kaggle](https://www.kaggle.com/victoropp).

Thanks for reading — and I welcome feedback, questions, or collaboration ideas.
