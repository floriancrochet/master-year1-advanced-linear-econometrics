# Econometric Analysis of Budget Management and Academic Success  
*A quantitative study on the financial determinants of students’ GPA in 2023–2024.*

---

## 📘 Overview
This project investigates the **impact of students’ financial management on their academic performance**.  
It was conducted as part of the **Master 1 in Econometrics and Statistics – Applied Econometrics track** at the University of Nantes.  

**Objectives**
- Quantify the relationship between students’ financial behavior and their overall grade average  
- Evaluate endogeneity issues and apply appropriate econometric methods  
- Provide evidence-based insights to improve student well-being and performance  

The study is based on a self-collected dataset from students in the Loire-Atlantique region, combining social, academic, and financial variables to model GPA outcomes.

---

## ⚙️ Features
- Linear econometric modeling using OLS and 2SLS (Two-Stage Least Squares)  
- Statistical validation: tests for normality, heteroskedasticity, multicollinearity, and endogeneity  
- Stepwise model selection and instrument relevance testing  
- Visualization of descriptive and regression results under R  
- Forecasting and interpretation of academic success determinants  

---

## 🧰 Tech Stack
**Language:** R  
**Libraries:** `openxlsx`, `car`, `MASS`, `tidyverse`, `EnvStats`, `lmtest`, `PerformanceAnalytics`, `corrplot`, `sjPlot`, `ggplot2`, `leaps`, `AER`  

---

## ⚙️ Installation

Clone the repository and ensure required R packages are installed:

```bash
git clone https://github.com/<your-username>/budget-econometrics.git
cd budget-econometrics
Rscript -e 'install.packages(c("openxlsx","car","MASS","tidyverse","EnvStats","lmtest","PerformanceAnalytics","corrplot","sjPlot","ggplot2","leaps","AER"))'
```

---

## 📚 Usage Example

```r
# Load data
Budget <- read.xlsx("data/budget.xlsx")

# Fit linear model
model <- lm(MOYENNE ~ ASSIDUITE + STRESS + RESTAURANT + EMPLOI + AGE, data = Budget)

# Display summary
summary(model)

# Plot residuals
plot(model$residuals)
```

Additional analyses and plots are included in the Quarto script `script économétrie linéaire avancée.qmd`.

---

## 📂 Project Structure

```
budget-econometrics/
│
├── data/                 # Collected survey data (budget.xlsx)
├── src/                  # Econometric scripts
│   └── script_econometrie_lineaire_avancee.R
├── results/              # Model outputs, tables, and figures
├── report/               # Final report (Pierre et Florian - dossier d'économétrie.pdf)
├── Projet_M1.pdf         # Assignment guidelines
└── README.md
```

---

## 📊 Results

Example result:  
The analysis reveals that **financial stress, number of restaurant visits, and student employment** negatively affect GPA, whereas **good health, tutoring participation, and external financial support** have a positive influence.  

Example visualization:  
![Distribution of GPA](./assets/gpa_distribution.png)

> Detailed graphs of model fit, residuals, and forecast diagnostics are provided in the R script output.

---

## 🧠 References
- Hamilton, *Time Series Analysis*  
- Wooldridge, *Introductory Econometrics: A Modern Approach*  
- Hyndman & Athanasopoulos, *Forecasting: Principles and Practice*  
- Lassarre et al. (2003). *Stress des étudiants et réussite universitaire.*  
- Verley & Zilloniz (2011). *Fragilités économiques, fragilités studieuses.*  
- Ministère de l’Enseignement Supérieur (2023). *Tableaux de réussite et passage par discipline.*  

---

## 📜 License
This project is released under the **MIT License**.  
© 2025 Pierre Quintin de Kercadio and Florian Crochet

---

## 👤 Authors
**Pierre Quintin de Kercadio**  
[GitHub Profile](https://github.com/PierreQDK)  

**Florian Crochet**  
[GitHub Profile](https://github.com/floriancrochet)

*Master 1 – Econometrics & Statistics, Applied Econometrics Track*

---

## 💬 Acknowledgments
Thanks to our professors and the open-source R community for their methodological guidance and tools that enabled this research.
