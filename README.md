# Churn MLOps Pipeline: CI/CD with GitHub Actions & CML

![Python](https://img.shields.io/badge/Python-3.11-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E.svg?style=flat&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458.svg?style=flat&logo=pandas&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF.svg?style=flat&logo=github-actions&logoColor=white)
![CML](https://img.shields.io/badge/CML-CC0000.svg?style=flat)

This repository implements an automated **CI/CD pipeline for Machine Learning**[cite: 4] using **GitHub Actions** and **CML (Continuous Machine Learning)**[cite: 4]. The project predicts customer churn while comparing different strategies to handle class imbalance[cite: 1].

---

## 🚀 Project Overview
In data science team workflows, tracking model performance across code modifications can be challenging[cite: 4]. This project automates the entire loop:
- **Push-triggered training:** Every `git push` automatically triggers a cloud runner to retrain the model[cite: 4].
- **Imbalance handling comparison:** Evaluates a baseline Random Forest (`without-imbalance`), a weighted approach (`with-class-weights`), and an oversampling technique (`with-SMOTE`)[cite: 8].
- **Automated CML Reporting:** Publishes performance metrics directly onto commits and Pull Requests.

---

## 🛠️ Tech Stack & Requirements
- **Language:** Python 3.11[cite: 5]
- **Libraries:** `scikit-learn`, `imbalanced-learn` (SMOTE), `pandas`, `numpy`, `matplotlib`, `seaborn`, `joblib`[cite: 6]
- **CI/CD & Automation:** GitHub Actions, CML (`iterative/setup-cml`)[cite: 10]
- **Environment:** Visual Studio Code[cite: 4], Git[cite: 4]

---

## 📂 Project Structure
```text
churn-cml/
├── .github/
│   └── workflows/
│       └── cml-churn.yaml   # GitHub Actions CI/CD pipeline configuration
├── dataset.csv              # Customer churn dataset[cite: 5]
├── script.py                # Data preprocessing, training, and metrics generation[cite: 5, 8]
├── requirements.txt         # Pinned python dependencies[cite: 5]
└── README.md
