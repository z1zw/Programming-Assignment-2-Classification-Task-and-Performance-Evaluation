# 🧠 Brain Tumor MRI Classification (Kaggle Programming Assignment)

This repository contains the code and experiment report for a brain tumor image classification assignment,  
conducted as part of the Programming Assignment on **Kaggle**.

🔗 **Kaggle Notebook Link:**  
👉 [https://www.kaggle.com/code/firstbuildzw/programming-assignment](https://www.kaggle.com/code/firstbuildzw/programming-assignment)

## 📂 Project Overview

The goal of this assignment is to classify brain MRI images into four categories:
- **glioma**
- **meningioma**
- **pituitary**
- **no tumor**

Early detection of brain tumors is a critical step in medical diagnosis, and this experiment compares multiple machine learning classifiers using image-based edge histogram features.

## ⚙️ Implemented

We implemented and compared **three classifiers** as assigned:

| # | Classifier | Implementation | Key Parameters |
|---|-------------|----------------|----------------|
| 1 | **Naive Bayes (GaussianNB)** | `sklearn.naive_bayes.GaussianNB()` | Default |
| 2 | **Neural Network (MLPClassifier)** | `sklearn.neural_network.MLPClassifier()` | hidden_layer_sizes=(10,10,10) |
| 3 | **Adaboost Classifier** | `sklearn.ensemble.AdaBoostClassifier()` | Default |

Additional model selection experiments were performed using **LinearSVC** with parameter sweep over `C = [0.1, 1, 10, 100]`.


## 📊 Dataset

**Dataset Source:** Combined from Figshare, SARTAJ, and Br35H datasets.  
- Total Images: **7,023**
- Split: **5,712 (train)** / **1,311 (test)**
- Images are categorized into 4 directories per class.

Each image was preprocessed and converted into **edge histogram descriptors** using Sobel filters.
