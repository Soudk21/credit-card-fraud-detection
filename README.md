# Credit Card Fraud Detection Using Machine Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Best Paper Award](https://img.shields.io/badge/🏆%20Best%20Paper%20Award-ICERAI-gold)](https://github.com/Soudk21/credit-card-fraud-detection)

## 📄 Abstract

This repository contains the implementation of our **ICERAI (Best Paper Award)** paper on credit card fraud detection. We present a systematic comparison of four classical machine learning classifiers — **Support Vector Machine (SVM)**, **Logistic Regression (LR)**, **K-Nearest Neighbors (KNN)**, and **XGBoost** — on a severely imbalanced real-world transaction dataset.

Our pipeline addresses extreme class imbalance (only **0.172%** fraud cases) through feature standardization and **Random UnderSampling** at a 1:2 fraud-to-legitimate ratio. All models are evaluated using accuracy, precision, recall, F1-score, and ROC-AUC. **XGBoost** achieved the highest discriminative power (**AUC = 0.98**), while **KNN** achieved the best accuracy-recall balance (**95.95% accuracy, 0.91 recall**).

## 📂 Repository Structure
