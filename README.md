# Econometric Analysis of Financial Management Impact on Academic Success
*This project analyzes the impact of students’ financial behavior on their academic performance using econometric modeling applied to survey data.*

---

## 🎯 Overview
This project investigates the impact of students’ financial behavior on their academic performance using econometric modeling applied to survey data collected from students in Loire-Atlantique (France) during the 2023–2024 academic year.

**Objectives**
- Identify key financial, social, and academic determinants of academic success.
- Apply linear econometric modeling with diagnostic and robustness tests.
- Evaluate the predictive performance of the estimated model.
- Provide policy recommendations to reduce financial stress among students.

---

## 🗄️ Data
- **Source:** Survey data collected from students in Loire-Atlantique (France).
- **Time Period:** 2023–2024 academic year.
- **Target Variable:** `MOYENNE` (Grade Point Average).
- **Key Predictors:** `ASSIDUITE`, `STRESS`, `RESTAURANT`, `AGE`, `SOMMEIL`, `TRAJET`.
- **Preprocessing:** Outlier detection and factor conversion.
- **Data Availability:** Survey data provided in `data/`.

---

## 🧠 Methodology
- **Theoretical Approach:** Linear Econometrics.
- **Mathematical Framework:** Ordinary Least Squares (OLS) and Two-Stage Least Squares (2SLS).
- **Evaluation Strategy:** Hypothesis testing (Normality, Heteroskedasticity, Multicollinearity) and specification testing.

---

## ⚙️ Features
- **Analyze Data Distributions:** Visualize univariate and bivariate distributions of academic and financial variables.
- **Model Academic Performance:** Estimate linear regression models to explain grade point averages.
- **Correct Endogeneity:** Apply instrumental variable approaches to address endogeneity in stress-related variables.
- **Validate Assumptions:** Test for normality, heteroskedasticity, and multicollinearity in regression residuals.

---

## 🧰 Tech Stack
- **Language:** R
- **Numerical Computing & Data Manipulation:** `tidyverse`, `openxlsx`, `leaps`
- **Econometrics & Statistical Inference:** `MASS`, `car`, `lmtest`, `AER`, `EnvStats`
- **Data Visualization:** `ggplot2`, `corrplot`, `sjPlot`, `PerformanceAnalytics`
- **Reporting & Documentation:** `Quarto`

---

## 📦 Installation

```bash
git clone https://github.com/À compléter/gestion-budget-etudiants.git
cd gestion-budget-etudiants
```

```R
install.packages(c("tidyverse", "MASS", "car", "lmtest", "AER",
                   "PerformanceAnalytics", "ggplot2", "sjPlot",
                   "corrplot", "EnvStats", "leaps", "openxlsx"))
```

---

## 💻 Usage Example

```r
library(openxlsx)
library(AER)

# Import dataset
Budget <- read.xlsx("data/student_budget_data_2023_2024.xlsx")

# Fit linear model
model <- lm(MOYENNE ~ ASSIDUITE + STRESS + RESTAURANT + AGE, data = Budget)
summary(model)

# Two-Stage Least Squares example
iv_model <- ivreg(MOYENNE ~ STRESS | CAF + LOGEMENT + SOMMEIL, data = Budget)
summary(iv_model)
```

---

## 📂 Project Structure

```text
master-year1-advanced-linear-econometrics/
│
├── data/
│   └── student_budget_data_2023_2024.xlsx
├── report/
│   └── report.pdf
├── LICENSE
├── README.md
├── master-year1-advanced-linear-econometrics.Rproj
└── project.qmd
```

---

## 📊 Results

### Key Findings
- Financial stress negatively impacts academic performance.
- Working while studying and frequent restaurant visits are associated with lower averages.
- Tutoring, scholarships, and financial support have a positive effect.
- Instrumental variables (CAF, rent, Uber Eats usage) effectively correct endogeneity in stress-related variables.

---

## 📚 References
- Hamilton, J.D. (1994). *Time Series Analysis*.
- Hyndman, R.J. & Athanasopoulos, G. (2018). *Forecasting: Principles and Practice.*
- Lassarre, D., Giron, C., & Paty, B. (2003). *Stress des étudiants et réussite universitaire*.
- Verley, E. & Zilloniz, S. (2011). *Fragilités économiques, fragilités studieuses.*
- Wooldridge, J.M. (2019). *Introductory Econometrics: A Modern Approach*.

---

## 📜 License
This project is released under the MIT License.
© 2025 Pierre Quintin de Kercadio & Florian Crochet

---

## 👤 Authors
**Pierre QUINTIN DE KERCADIO**
[GitHub Profile](https://github.com/PierreQDK)

**Florian CROCHET**
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track*

---

## 🤝 Acknowledgments
This work was conducted as part of the Advanced Linear Econometrics course, supervised by Muriel Travers. We thank the students who participated in the survey.
