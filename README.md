# Credit Card Fraud Detection Using Machine Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![Best Paper Award](https://img.shields.io/badge/🏆%20Best%20Paper%20Award-ICERAI-gold)](https://aurak.ac.ae/icerai-2026)

## 📄 Abstract

This repository contains the implementation of our **ICERAI (Best Paper Award)** paper on credit card fraud detection. We present a systematic comparison of four classical machine learning classifiers — **Support Vector Machine (SVM)**, **Logistic Regression (LR)**, **K-Nearest Neighbors (KNN)**, and **XGBoost** — on a severely imbalanced real-world transaction dataset.

Our pipeline addresses extreme class imbalance (only **0.172%** fraud cases) through feature standardization and **Random UnderSampling** at a 1:2 fraud-to-legitimate ratio. All models are evaluated using accuracy, precision, recall, F1-score, and ROC-AUC. **XGBoost** achieved the highest discriminative power (**AUC = 0.98**), while **KNN** achieved the best accuracy-recall balance (**95.95% accuracy, 0.91 recall**).

## 📂 Repository Structure

```bash
├── data/
│   └── README.md                        # Kaggle dataset link and description
├── notebooks/
│   └── fraud_detection_svm_knn_lr_xgboost.ipynb  # Full pipeline notebook
├── paper/
│   └── Credit_Card_Fraud_Detection_ICERAI.pdf     # Published conference paper
├── LICENSE
├── README.md
└── requirements.txt
```
---

This is the official code for the ICERAI paper:
**Credit Card Fraud Detection Using Machine Learning Techniques**
Authors: Soud Asaad, Omer Farooq, Almotaz Al Muntaser, Mohammad Azmi Al-Betar (Ajman University, UAE)
[Download Paper (PDF)](./paper/Credit_Card_Fraud_Detection_ICERAI.pdf)

---

## ⚙️ Methodology

- **Preprocessing:** Drop `Time` feature, standardize `Amount` via z-score normalization
- **Class Balancing:** Random UnderSampling at 1:2 fraud-to-legitimate ratio (training set only)
- **Train/Test Split:** 80/20 stratified split with fixed random state for reproducibility
- **Classifiers:** SVM (RBF kernel), Logistic Regression, KNN (k=3), XGBoost
- **Evaluation:** Accuracy, Precision, Recall, F1-score, ROC-AUC, Confusion Matrices

## 📊 Results

| Model | Accuracy | Precision | Recall | F1 Score | AUC |
|---|---|---|---|---|---|
| SVM | 94.59% | 0.989 | 0.861 | 0.921 | 0.977 |
| Logistic Regression | 95.27% | 0.970 | 0.898 | 0.933 | 0.976 |
| KNN (k=3) | 95.95% | 0.980 | 0.907 | 0.942 | 0.971 |
| XGBoost | 95.61% | 0.980 | 0.898 | 0.937 | **0.980** |

> XGBoost achieved the highest AUC (0.98), while KNN achieved the best accuracy-recall balance.

## 🗃️ Dataset

The dataset used is the [Credit Card Fraud Detection dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) from Kaggle.

- 284,807 transactions over two days (September 2013, European cardholders)
- 492 fraud cases — only **0.172%** of all transactions
- Features V1–V28 are PCA-transformed for anonymization
- See `data/README.md` for details

> ⚠️ The dataset is not included in this repository due to size. Download it directly from Kaggle.

## 🚀 Installation

```bash
git clone https://github.com/Soudk21/credit-card-fraud-detection.git
cd credit-card-fraud-detection
pip install -r requirements.txt
```

## 📓 Usage

Open the notebook and run all cells:

```bash
jupyter notebook notebooks/fraud_detection_svm_knn_lr_xgboost.ipynb
```

Make sure you download the dataset from Kaggle and place `creditcard.csv` inside the `data/` folder before running.

## 🤝 Acknowledgments

- Dataset: [ULB Machine Learning Group](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) via Kaggle
- Affiliated with: Artificial Intelligence Research Center (AIRC), Ajman University, UAE

## 📜 Citation

If you use this code or findings in your research, please cite:

```bibtex
@inproceedings{asaad2025creditcard,
title={Credit Card Fraud Detection Using Machine Learning Techniques},
author={Asaad, Soud and Farooq, Omer and Al Muntaser, Almotaz and Al-Betar, Mohammad Azmi},
booktitle={Proceedings of ICERAI},
year={2025}
}

```

## License

MIT License. See [LICENSE](./LICENSE) for details.
