# ⚽ A2 — FIFA 24 Player Market Value Prediction
### Feedforward Neural Network · Ligue 1 · EA Sports FC 24 Dataset · VS Code · Python 3.11.15

---

## 📌 Project Overview

This project predicts the market value (`value_eur`) of **Ligue 1 football players** using in-game statistics from the EA Sports FC 24 dataset. The pipeline spans Exploratory Data Analysis, IQR-based outlier removal, multi-method feature selection, Structural Equation Modeling (SEM), KMeans clustering, and a Feedforward Neural Network (FFNN) for final predictions.

> 🔄 **Status: In Progress**

---

## 📊 Dataset

- **Source:** EA Sports FC 24 Dataset
- **Target Variable:** `value_eur` — player market value in euros
- **Scope:** Ligue 1 players only

| Stage | Rows | Columns |
|---|---|---|
| Full FIFA 24 Dataset | 180,021 | 109 |
| Filtered to Ligue 1 | 5,088 | 109 |
| After dropping null `value_eur` | 5,080 | 109 |
| After IQR outlier removal | 4,458 | 110 |

---

## 🔄 Pipeline

**1. 📊 Exploratory Data Analysis (EDA)**
Understanding distributions, correlations, and missing values across 109 features before any modeling begins.

**2. 🧹 Data Cleaning**
- Filtered full dataset to Ligue 1 players only
- Removed rows with null `value_eur`
- Applied **IQR-based outlier removal** to reduce noise and improve model generalization

**3. 🔍 Feature Selection**
Three methods were applied and compared to identify the **top 4 most predictive features:**

| Method | Approach |
|---|---|
| **KBest** | Selects features with highest statistical scores (f_regression) |
| **LASSO** | Penalizes less important features, shrinking coefficients to zero |
| **Decision Tree** | Ranks features by impurity-based importance scores |

**4. 🏗️ Structural Equation Modeling (SEM)**
SEM builds **latent constructs** from groups of correlated in-game variables, capturing deeper relationships that individual features alone cannot express.

Example constructs:
- **Technical Skill** — dribbling, ball control, short passing, vision
- **Physical Ability** — pace, stamina, strength, acceleration

**5. 🔵 KMeans Clustering**
Reveals distinct **player archetypes** within Ligue 1 by grouping players according to their in-game attribute profiles.

**6. 🧠 Feedforward Neural Network (FFNN)**
Final model trained on a proper Train/Test split to predict continuous market value.

---

## 🧠 Model — Feedforward Neural Network (FFNN)

- **Task:** Regression — predicting continuous `value_eur`
- **Architecture:** Fully connected layers with ReLU activations
- **Split:** Train / Test
- **Framework:** PyTorch

> ⚙️ Final architecture, hyperparameters, and evaluation metrics will be updated upon project completion.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.11.15-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0-orange)
![VSCode](https://img.shields.io/badge/VS_Code-Editor-007ACC?logo=visualstudiocode)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-latest-green)

| Tool | Purpose |
|---|---|
| Python 3.11.15 | Core programming language |
| PyTorch | FFNN model building & training |
| Scikit-learn | Feature selection, KMeans clustering, preprocessing |
| SEM | Latent construct modeling |
| VS Code | Development environment |
| GitHub | Version control & portfolio hosting |

---

## 🚀 How to Run

1. Clone the repository
```bash
git clone https://github.com/Jalfaro704/Portafolio-AML.git
cd Portafolio-AML
```
2. Make sure you have **Python 3.11.15** installed
3. Install dependencies
```bash
pip install -r requirements.txt
```
4. Open the project in **VS Code** and run the notebook or script

---

## 📈 Roadmap

- [ ] EDA & Data Cleaning *(in progress)*
- [ ] Feature Selection — KBest, LASSO, Decision Tree
- [ ] SEM Latent Construct Modeling
- [ ] KMeans Clustering
- [ ] FFNN Training & Evaluation
- [ ] Final Results & Model Export

---

## 🤝 Connect

Feel free to follow along, star the repo, or reach out — always happy to connect with others learning ML.

[![GitHub](https://img.shields.io/badge/GitHub-Jalfaro704-black?logo=github)](https://github.com/Jalfaro704)

---

*Built with 🧠 during Advanced Machine Learning coursework · Python 3.11.15 · VS Code*
