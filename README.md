# 🧠 Portafolio-AML — Machine Learning Portfolio
### Advanced Machine Learning | PyTorch · Python · Real-World Datasets

---

## 👋 About This Portfolio

This repository serves as the central hub for all Machine Learning projects developed during my **Advanced Machine Learning** coursework. Each project applies end-to-end ML workflows — from data cleaning and feature engineering to model training, tuning, and evaluation — using real-world datasets.

New projects are added each sprint. All code is written in Python and trained on GPU-accelerated environments (Google Colab T4).

---

## 📂 Projects

| # | Project | Description | Stack | Status |
|---|---|---|---|---|
| A2 | [FIFA 24 Player Market Value Predictor](#a2--fifa-24-player-market-value-prediction-in-progress) | FFNN to predict Ligue 1 player market values using feature selection, SEM & KMeans | PyTorch · Scikit-learn · SEM | 🔄 In Progress |

---

## A2 — FIFA 24 Player Market Value Prediction *(In Progress)*

**Goal:** Predict the market value (`value_eur`) of Ligue 1 football players using in-game statistics from the EA Sports FC 24 dataset.

**Pipeline:**
1. 📊 **Exploratory Data Analysis (EDA)** — understanding distributions, correlations, and missing values
2. 🧹 **Data Cleaning** — IQR-based outlier removal, null value handling
3. 🔍 **Feature Selection** — KBest, LASSO, and Decision Tree methods to identify top 4 predictive features
4. 🏗️ **Structural Equation Modeling (SEM)** — builds latent constructs (e.g., Technical Skill, Physical Ability) from correlated variables
5. 🔵 **KMeans Clustering** — reveals distinct player archetypes within Ligue 1
6. 🧠 **Feedforward Neural Network (FFNN)** — trained on Train/Test split to predict market value

**Tech Stack:** PyTorch · Scikit-learn · SEM · KMeans · Python · Google Colab

**Dataset:**

| Stage | Rows | Columns |
|---|---|---|
| Full FIFA 24 Dataset | 180,021 | 109 |
| Filtered to Ligue 1 | 5,088 | 109 |
| After dropping null `value_eur` | 5,080 | 109 |
| After IQR outlier removal | 4,458 | 110 |

**Expected Outcome:** A model capable of accurately estimating a Ligue 1 player's economic worth while identifying which latent constructs and individual features drive that value most.

📁 **File:** `A2_FIFA24_FFNN.ipynb` *(coming soon)*

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.12-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-orange)
![Colab](https://img.shields.io/badge/Google_Colab-T4_GPU-yellow)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-latest-green)

| Tool | Purpose |
|---|---|
| PyTorch | CNN & FFNN model building |
| Torchvision | Dataset loading & image transforms |
| Scikit-learn | Feature selection, clustering, preprocessing |
| SEM | Latent construct modeling |
| Google Colab | GPU-accelerated training (T4) |
| GitHub | Version control & portfolio hosting |

---

## 🚀 How to Run Any Project

1. Open the `.ipynb` file in **Google Colab**
2. Go to `Runtime → Change runtime type → T4 GPU`
3. Run all cells in order
4. Models are saved automatically to Google Drive

---

## 📈 Roadmap

- [x] A1 — CNN Binary Image Classifier
- [ ] A2 — FIFA 24 FFNN Market Value Predictor
- [ ] A3 — *(Coming next sprint)*

---

## 🤝 Connect

Feel free to follow along, star the repo, or reach out — always happy to connect with others learning ML.

[![GitHub](https://img.shields.io/badge/GitHub-Jalfaro704-black?logo=github)](https://github.com/Jalfaro704)

---
