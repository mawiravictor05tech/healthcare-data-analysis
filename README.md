# Healthcare Treatment and Patient Recovery Analysis

![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![Data Analysis](https://img.shields.io/badge/Focus-Data%20Science-orange.svg)
![Statistical Testing](https://img.shields.io/badge/Stats-ANOVA%20%2F%20Hypothesis-green.svg)

## Project Description
This repository features a comprehensive Python data analysis of healthcare data. It evaluates structural factors like patient age, clinical severity, and drug dosage metrics across separate treatment groups to effectively model and determine the exact key influences impacting physical recovery timelines. 

The study leverages rigorous exploratory data analysis (EDA), summary statistics, and formal parametric hypothesis testing (ANOVA) to validate whether chosen medical interventions significantly alter patient rehabilitation speed.

---

## Repository Contents
* **`Untitled18.ipynb`**: The primary Jupyter Notebook containing the full data pipeline, calculations, data visualization scripts, and statistical test execution.
* **`healthcare_dataset_.xlsx`**: The clinical dataset comprising 250 unique patient profiles and structural treatment metrics.

---

## Dataset Architecture
The data includes 250 clinical records with the following structural dimensions:
* `patient_id`: Unique identifier for each tracked subject.
* `age`: Age of the patient (ranging from 20 to 79 years).
* `severity_score`: Objective clinical baseline index of the condition (Scale: 1.0 - 10.0).
* `dosage_mg`: Quantified medication volume administered (mg).
* `treatment_type`: Categorical tracking of physical recovery interventions (`Medication_A`, `Medication_B`, `Physiotherapy`).
* `recovery_days`: The target metric capturing the total number of days taken to achieve medical recovery.

---

## Analytical & Statistical Pipeline

### 1. Exploratory Data Analysis (EDA)
* Calculates key metrics of central tendency (Mean, Median, Mode) across patient populations.
* Profiles distribution spreads and standard deviations to highlight variable variations (e.g., patient age exhibits the highest standard deviation in this population).
* Generates continuous data distribution plots using `seaborn` and `matplotlib`.

### 2. Hypothesis Testing (ANOVA)
To determine if different treatment methodologies systematically impact recovery timelines, a One-Way Analysis of Variance (ANOVA) was executed using the following parameters:
* **Null Hypothesis ($H_0$):** The type of treatment has no significant effect on the patient `recovery_days`.
* **Alternative Hypothesis ($H_1$):** The type of treatment has a significant effect on the patient `recovery_days`.

**Test Output:**
* **F-statistic:** 129.5000
* **P-value:** 0.0016

*Conclusion:* Given that the $P\text{-value} < 0.05$, we reject the null hypothesis ($H_0$) in favor of the alternative ($H_1$), proving that the selection of treatment type yields a statistically significant difference in patient recovery speed.

---

## Setup & Execution

### Prerequisites
Ensure you have Python 3.8+ and the following data science libraries installed:
```bash
pip install pandas openpyxl matplotlib seaborn scipy
