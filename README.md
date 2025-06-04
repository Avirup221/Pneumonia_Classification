# Pneumonia Classification Using Machine Learning

This repository contains the code and report for a project focused on classifying chest X-ray images to detect pneumonia using various machine learning algorithms. The project compares models like SVM (Linear, Polynomial, RBF), Decision Trees, Random Forests, Bagging, and a Voting Classifier.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Motivation](#motivation)
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Algorithms Used](#algorithms-used)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Installation](#installation)
- [How to Run](#how-to-run)
- [Future Work](#future-work)
- [Contributors](#contributors)

---

## 🧠 Project Overview

Pneumonia is a serious respiratory condition and timely diagnosis can save lives. This project leverages machine learning models to automate the classification of chest X-ray images into:
- **Normal**
- **Pneumonia** (bacterial or viral)

The goal is to develop a scalable and accessible diagnostic tool for use in under-resourced medical environments.

---

## 💡 Motivation

Manual diagnosis using chest X-rays is time-consuming and prone to human error. In low-income regions, radiologists are often unavailable. This project aims to:
- Provide an AI-assisted diagnostic tool
- Improve speed and accuracy of detection
- Demonstrate the power of ML in healthcare

---

## 📂 Dataset

- **Source:** [Kaggle - Chest X-ray Images (Pneumonia)](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)
- **Classes:** `NORMAL`, `PNEUMONIA`
- **Data Split:** Train / Validation / Test
- **Preprocessing Includes:**
  - Resizing to 64x64
  - Grayscale conversion
  - Normalization
  - Flattening
  - Class balancing (2000 samples each)

---

## 🛠 Preprocessing

- Libraries: `OpenCV`, `NumPy`, `Pandas`, `Matplotlib`, `Seaborn`
- Techniques:
  - Image augmentation
  - Brightness analysis
  - Dataframe generation with full file paths
  - Shuffling and balancing the dataset
  - Visualizations (sample images, label distributions)

---

## 🤖 Algorithms Used

- **Support Vector Machines (SVM):**
  - Linear Kernel
  - Polynomial Kernel
  - RBF Kernel
- **Decision Tree**
- **Random Forest**
- **Bagging (with Decision Tree)**
- **Voting Classifier** (ensemble of all models)

Hyperparameter tuning was performed using `GridSearchCV`.

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **ROC Curve & AUC**

---

## 🏆 Results (on Test Set)

| Model                  | Accuracy | Precision | Recall | F1-Score |
|------------------------|----------|-----------|--------|----------|
| SVM (Linear)           | 0.76     | 0.74      | 0.98   | 0.84     |
| SVM (Polynomial)       | 0.76     | 0.76      | 0.98   | 0.85     |
| SVM (RBF)              | 0.77     | 0.93      | 0.42   | 0.58     |
| Decision Tree          | 0.75     | 0.75      | 0.91   | 0.82     |
| Random Forest          | **0.86** | 0.83      | 0.97   | **0.89** |
| Bagging Classifier     | 0.81     | 0.80      | 0.95   | 0.86     |
| Voting Classifier      | 0.79     | 0.76      | 0.98   | 0.86     |

---

## 🧰 Installation

```bash
git clone https://github.com/your-username/pneumonia-classification.git
cd pneumonia-classification
