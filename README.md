# Recommendation System Project

## Team Members
- Dana Alnemari
- Sarah Sadik
- Jana Alharbi

---

# Project Overview

This project focuses on Sequential Recommendation Systems using Transformer-based recommendation models.

The main goal of the project is to reproduce and evaluate the research paper:

**“Attention Calibration for Transformer-based Sequential Recommendation (AC-TSR)”**

Instead of using the original datasets from the paper, we applied the models on a different dataset and conducted our own experiments, analysis, tuning, and evaluations.

The project was implemented using the RecBole framework and deep learning recommendation models.

---

# Paper Idea

The paper discusses a problem in Transformer-based recommender systems such as SASRec.

The authors found that:
- Attention mechanisms sometimes give high attention weights to irrelevant items.
- This can reduce recommendation accuracy.

To solve this problem, the paper introduced:
- Spatial Calibrator
- Adversarial Calibrator

These components help the model focus more on important user interactions and improve recommendation quality.

---

# What We Implemented

In this project, we:
- Implemented and trained sequential recommendation models.
- Reproduced experiments inspired by the research paper.
- Applied the models on a different dataset from the original paper.
- Compared the performance of:
  - SASRec
  - AC-SASRec
- Evaluated the models using recommendation metrics.

---

# Our Contributions and Modifications

We did not directly copy the paper implementation.  
We added several experiments and modifications, including:

## 1. Hyperparameter Tuning

We tuned multiple parameters such as:
- Learning rate
- Hidden size
- Number of attention heads
- Number of layers
- Dropout rate
- Batch size
- Epochs

to improve recommendation performance.

---

## 2. Additional Evaluation Metrics

We evaluated the models using:
- Hit@10
- Hit@20
- Recall@10
- Recall@20
- MRR@10
- MRR@20
- NDCG@10
- NDCG@20

---

## 3. Ablation Study

We performed an ablation study on AC-SASRec by removing one calibration component at a time to analyze its impact on recommendation performance.

The experiments included:
- Without Order Calibration
- Without Distance Calibration
- Without Adversarial Calibration

The results showed that the full AC-SASRec model achieved the best overall performance.

---

## 4. Overfitting Analysis

We monitored:
- Training loss
- Validation metrics
- Epoch behavior

to study overfitting and model generalization.

---

## 5. Model Comparison

We compared:
- SASRec and AC-SASRec
- The baseline version of AC-SASRec with the tuned version after hyperparameter tuning

to analyze the impact of attention calibration and hyperparameter tuning on recommendation performance.

---

# Dataset

The project uses a recommendation dataset containing user-item interactions for sequential recommendation tasks.

Dataset link:  
https://www.kaggle.com/datasets/saurabhbagchi/amazon-electronics-data/code

The dataset was preprocessed before training by:
- Cleaning data
- Encoding interactions
- Preparing sequential inputs
- Splitting into train/validation/test sets

---

# Technologies Used

- Python
- PyTorch
- RecBole
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

# How to Run the Project

1. Open the notebook file.
2. Install the required libraries.
4. Upload the dataset.
5. Run the notebook cells in order.
6. Train and evaluate the models.

---

# Main Objective

The main objective of this project is to analyze how attention calibration can improve Transformer-based sequential recommendation systems and compare the recommendation performance between baseline and improved models.

---

# Reference

Peilin Zhou et al.  
**“Attention Calibration for Transformer-based Sequential Recommendation”**  
CIKM 2023.

---

# Important Note

It is highly recommended to run this project using GPU acceleration (such as Google Colab GPU or CUDA-supported environments), since training Transformer-based recommendation models can take a significant amount of time on CPU.

Using GPU will greatly improve:
- Training speed
- Model performance experimentation
- Hyperparameter tuning efficiency

Recommended environments:
- Google Colab GPU
- Kaggle Notebook GPU
- Local machine with NVIDIA GPU
