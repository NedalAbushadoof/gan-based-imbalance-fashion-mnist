# Balancing Imbalanced Image Datasets Using GAN Variants  
### A Case Study on Fashion-MNIST

## 📌 Project Overview
Class imbalance is a common challenge in machine learning that often leads to biased classifiers.  
This project explores the use of **Generative Adversarial Networks (GANs)** to address class imbalance in image classification tasks.

We compare:
- **Vanilla GAN**
- **Wasserstein GAN with Gradient Penalty (WGAN-GP)**

for generating synthetic samples of a minority class and evaluate their impact on classification performance.

---

## 📊 Dataset
- **Fashion-MNIST**
- 70,000 grayscale images (28×28)
- 10 clothing categories
- **Minority class:** Sneaker (class 7)
- Artificial imbalance introduced by downsampling the Sneaker class

---

## 🧠 Methodology

### 1️⃣ GAN-Based Data Augmentation
- Vanilla GAN trained on minority class only
- WGAN-GP trained on minority class only
- Synthetic samples generated to balance the dataset to the **average class size**

### 2️⃣ Classification
- CNN classifier
- Trained under three scenarios:
  1. Original imbalanced dataset
  2. Balanced using Vanilla GAN
  3. Balanced using WGAN-GP

---

## 📈 Evaluation Metrics
- Accuracy
- Precision (Macro)
- Recall (Macro)
- F1-Score (Macro)
- AUC-ROC
- Confusion Matrix

---

## ✅ Key Findings
- Vanilla GAN provides limited improvement due to unstable training
- WGAN-GP produces higher-quality synthetic samples
- GAN-based augmentation improves minority class balance
- Overall accuracy remains stable while class fairness improves

---

## 📁 Repository Structure
