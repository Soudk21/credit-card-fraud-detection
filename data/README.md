# Dataset

## Credit Card Fraud Detection Dataset

The dataset used in this project is the **Credit Card Fraud Detection** dataset,
publicly available on Kaggle.

🔗 [Download from Kaggle](https://www.kaggle.com/datasets/mlgulb/creditcardfraud)

---

## Description

| Property | Details |
|---|---|
| Source | Kaggle / ULB Machine Learning Group |
| Transactions | 284,807 |
| Fraud cases | 492 (0.172%) |
| Time period | 2 days, September 2013 |
| Cardholders | European |
| Missing values | None |

## Features

| Feature | Description |
|---|---|
| `Time` | Seconds elapsed since first transaction (dropped in preprocessing) |
| `Amount` | Transaction amount in Euros (standardized to `std_Amount`) |
| `V1–V28` | PCA-transformed anonymized features |
| `Class` | Target label — 0: legitimate, 1: fraud |

## Usage

Download `creditcard.csv` from Kaggle and place it in this `data/` folder
before running the notebook:
