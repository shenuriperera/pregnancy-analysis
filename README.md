# Pregnancy Data Analysis

Statistical analysis of pregnancy data to identify key factors influencing **infant birth weight**, using Multiple Linear Regression and Ordinal Regression in R.

---

## 📌 Project Overview

This project analyzes a dataset of **1,236 pregnancies** from the San Francisco East Bay area (1960–1967) to investigate how maternal and pregnancy factors affect infant birth weight.

---

## 🎯 Objectives

- Identify influential factors on infant birth weight
- Examine the most important factors for keeping birth weight in a healthy range (88–141 ounces)
- Build regression models that maximize R² without overfitting

---

## 📊 Dataset

| Variable | Description |
|----------|-------------|
| `bwt` | Birth weight of the baby (ounces) |
| `gestation` | Length of gestation (days) |
| `parity` | First pregnancy indicator (0 = first, 1 = not first) |
| `age` | Mother's age (years) |
| `height` | Mother's height (inches) |
| `weight` | Mother's weight (pounds) |
| `smoke` | Smoking status (0 = No, 1 = Yes) |

**Source:** [Kaggle - Babies Birth Weight](https://www.kaggle.com/datasets/debjeetdas/babies-birth-weight)

---

## 🔬 Methods

### 1. Multiple Linear Regression (MLR)
- Forward selection used to identify significant predictors
- Interaction terms and polynomial terms added to improve R²
- Multicollinearity checked using VIF values
- Residual analysis conducted to verify model assumptions

**Final MLR Model:**
```
bwt = (-59.01) + 0.370*gestation + (-66.72)*smoke + 1.147*height
      + (-3.301)*parity + 0.046*weight + 0.209*(smoke*gestation)
```
> R² = 26.55%

### 2. Ordinal Regression
- Birth weight classified into 3 categories:
  - **Underweight:** < 88 ounces
  - **Normal weight:** 88–141 ounces
  - **Overweight:** > 141 ounces
- Forward selection used to fit the ordinal model
- Interaction term (gestation × smoke) added to improve deviance

---

## 📈 Key Findings

- **Gestation period** is the strongest predictor of birth weight
- **Smoking** negatively impacts birth weight
- **Mother's height** has a weak positive correlation with birth weight
- **Age** was found to be statistically insignificant

---

## 🛠️ Technologies Used

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)

**Libraries:** `car`, `MASS`, `ordinal`

---

## 👥 Contributors

| Student | Contribution |
|---------|-------------|
| D.G. Sandani Gunasekara (S16903) | MLR Analysis, Discussion & Adequacy of Findings |
| H.S.S. Perera (S16661) | Ordinal Regression, Discussion & Adequacy of Findings |
| W.A.D. Fernando (S16979) | Literature Review & Ordinal Regression |
| J.B.A.A.Y. Dharmasena (S16938) | Introduction & Descriptive Data Analysis |
| O.S. Jayathunga (S16807) | Descriptive Analysis, Literature Review & Conclusion |

---

## 📁 Repository Structure

```
pregnancy-analysis/
├── group3.R          # Full R analysis script
├── babies.csv        # Dataset
└── README.md         # Project documentation
```

---

*ST 3011 | Department of Statistics | G.C.E. A/L 2020 Sri Lanka*
