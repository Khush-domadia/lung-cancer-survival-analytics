# 🫁 Lung Cancer Survival Analytics

## 📌 Project Overview
This project presents an end-to-end **oncology survival analysis** integrating **clinical staging**, **treatment patterns**, **molecular biomarkers**, and **penalized Cox proportional hazards modeling** to identify key drivers of mortality risk in lung cancer patients.

The analysis combines **exploratory clinical analytics**, **survival distribution analysis**, and **regularized survival modeling**, culminating in an **interactive Tableau dashboard** designed for clinical and stakeholder interpretation.

---

## 🎯 Objectives
- Quantify survival outcomes across **TNM 8th edition cancer stages**
- Evaluate **treatment intensity patterns** by disease progression
- Assess the relationship between **smoking behavior** and **oncogenic mutations (EGFR, KRAS)**
- Identify **high-impact clinical and molecular predictors** of mortality using penalized Cox regression
- Translate statistical findings into **clinically interpretable visual insights**

---

## 🧬 Data Description
The dataset includes patient-level oncology records with:
- **Demographics:** Age, Sex
- **Clinical variables:** TNM stage, tumor grade, tumor size
- **Treatment modalities:** Chemotherapy, Chemoradiation, Radiation therapy, No adjuvant therapy
- **Molecular biomarkers:** EGFR mutation status, KRAS mutation status
- **Behavioral factors:** Smoking status, pack-years
- **Outcomes:** Survival time (days/years), mortality event indicator

---

## 📊 Analytical Workflow

### 1️⃣ Exploratory Clinical Analysis
**Notebook:** `Healthcare_data_visualization.ipynb`

- Stage-wise treatment distribution analysis
- Survival distribution visualization using box-and-whisker plots
- Mutation prevalence stratified by smoking status
- Cohort-level KPIs including:
  - Total patient count
  - Overall mortality rate
  - Median survival time

---

### 2️⃣ Survival Modeling
**Notebook:** `Survival_model.ipynb`

- Implemented **penalized Cox proportional hazards regression (L2 regularization)**
- Addressed:
  - Small subgroup instability
  - Multicollinearity among clinical covariates
- Estimated:
  - Log hazard ratios
  - Hazard ratios with confidence intervals
- Ranked predictors by **absolute effect size** to identify dominant mortality drivers

---

## 📈 Key Findings (Measurable Results)

- **Treatment intensity increased with advancing stage**, yet survival distributions showed substantial overlap across stages, highlighting biological heterogeneity.
- **Smoking status strongly correlated with KRAS mutation prevalence**, while EGFR mutations were enriched in never-smokers.
- Penalized Cox modeling identified **advanced stage, KRAS mutation, and lack of adjuvant therapy** as high-impact mortality risk factors.
- Median survival varied by stage by **over 3 years**, while molecular features explained additional mortality risk beyond staging alone.
- Regularization improved model stability and interpretability in a **small-sample clinical dataset**.

---

## 📊 Interactive Dashboard
An interactive Tableau dashboard was developed to enable:
- Stage-level filtering of survival outcomes
- Exploration of mutation patterns by smoking behavior
- Visual interpretation of Cox model hazard ratios

🔗 **Tableau Public Dashboard:**
[Clinical Molecular and Survival Patterns in Lung Cancer](https://public.tableau.com/app/profile/khush.domadiya/viz/ClinicalMolecularandSurvivalPatternsinLungCancer/Dashboard2?publish=yes)

---

## 🛠️ Tools & Technologies
- **Python:** pandas, numpy, lifelines, matplotlib, seaborn
- **Survival Analysis:** Cox proportional hazards, L2 penalization
- **Visualization:** Tableau Public
- **Version Control:** Git, GitHub
- **Domain:** Oncology, clinical outcomes analytics, precision medicine

---

## 📁 Repository Structure

```
lung-cancer-survival-analytics/
├── Healthcare_data_visualization.ipynb
├── Survival_model.ipynb
├── data/
│   └── *.csv
├── tableau/
│   └── *.twb / *.twbx
└── README.md
```

---

## 🧠 Clinical & Business Impact
This project demonstrates the ability to:
- Translate **clinical oncology data** into actionable insights
- Apply **advanced survival modeling** in real-world healthcare datasets
- Communicate complex statistical results to **non-technical stakeholders**
- Support **evidence-based decision-making** in oncology and precision medicine

---

## 📌 Notes
- Cox model uses **L2 penalization** to mitigate overfitting and separation in small clinical subgroups.
- Analysis is intended for **educational and analytical demonstration purposes**.
