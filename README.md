# Student Loans Data Mining: Classifying High Default Risk in U.S. College Programs

### *Analysis of College Scorecard Data for Predicting High Default Risk*

**Authors:** Brian Hunt, Logan Laszewski, Eliza Shane
**Course:** Data Mining Project – Elon University (2025)

---

## Overview

This project uses U.S. Department of Education College Scorecard data to classify higher education programs by their risk of student loan default. Using both **Logistic Regression (Lasso, Ridge, ElasticNet)** and **Random Forest**, we identify programs and institutional characteristics most associated with high default rates.

We focus on:

* Program-level risk analysis
* Institutional factors (type, region, online availability)
* Major category impacts on default probability

---

## Purpose of This Project

* Address the financial and institutional challenges posed by student loan defaults
* Inform policy and student decision-making through predictive modeling
* Develop reproducible data mining workflows on large government datasets
* Gain experience in:

  * Data cleaning, merging, and preprocessing
  * Feature engineering
  * Classification modeling with linear and non-linear methods
  * Model evaluation using precision, recall, F1-score
  * Data visualization for actionable insights

---

## Skills Demonstrated

* **Data Cleaning & Preparation:** Python (Pandas, NumPy), handling missing and suppressed data, categorical encoding
* **Feature Engineering:** Creating ratios (e.g., debt-to-income), binary classification labels, dummy variables
* **Modeling:** Logistic Regression (Ridge, Lasso, ElasticNet), Random Forest Classifier
* **Evaluation & Visualization:** Confusion matrices, precision-recall curves, feature importance, Matplotlib, Seaborn, Plotly
* **Interpretability:** Regression coefficients, permutation importance, Ridge/Lasso coefficient plots

---

## Research Questions

* Which types of educational programs are most associated with future loan defaults?
* What institutional characteristics indicate high default risk early?
* How do degree type, major, region, and control type affect default probabilities?

---

## Methods Summary

### Dataset

* **Field of Study Level:** Most-Recent-Cohorts-Field-of-Study.csv
* **Institution Level:** Most-Recent-Cohorts-Institution.csv
* **Data Dictionary:** Dictionary and Data Sets.zip

### Data Cleaning Steps

* Merge datasets on `UNITID`
* Remove privacy-suppressed (`PS`) and missing values
* Categorize majors into broad CIPDESC categories
* Encode categorical variables (degree type, major category, region)
* Transform `BBRR3_FED_COMP_DFLT` into binary classification (`high_default` >10% default)
* Feature engineering (DEBT_TO_INCOME, distance education coding, main campus status)

### Modeling

* **Logistic Regression:** Lasso, Ridge, ElasticNet for interpretable coefficients
* **Random Forest:** Ensemble method to capture complex non-linear patterns
* **Evaluation:** Precision, recall, F1-score, permutation feature importance, confusion matrices

### Software

* Python
* Packages: Pandas, NumPy, Scikit-learn, Statsmodels, Matplotlib, Seaborn, Plotly

---

## Key Results

* **Degree Type:** Undergraduate certificates/diplomas most at risk, Bachelor’s degrees most stable
* **Major Categories:** Vocational & Technical, Engineering & Technology, Arts & Humanities have higher defaults
* **Institution Type:** Private schools show higher default rates than public
* **Region:** Plains and Great Lakes regions show elevated risk
* **Distance Education:** Fully online programs show mixed risk patterns

**Business Recommendations:**

1. Implement dashboards for students to assess program-level default risk
2. Institutions can focus advising and support on high-risk programs
3. Policymakers can monitor programs that exceed threshold defaults

---

## Next Steps

* Update models with the latest College Scorecard data
* Explore advanced ensemble models (XGBoost, LightGBM)
* Consider individual-level analysis using anonymized datasets

---

## Limitations

* Program-level analysis; individual outcomes may vary
* Privacy-suppressed (`PS`) data limits completeness
* Correlational analysis, causality not guaranteed
* Potential biases from demographics and region

---

## Documents

* Final Paper: [Written Report.docx](./Written Report.docx)
* Code Notebook: [The_Gamblers_Final_Version_1.ipynb](./The_Gamblers_Final_Version_1.ipynb)
* Data Dictionary & Datasets: [Dictionary and Data Sets.zip](./Dictionary and Data Sets.zip)

---

## Acknowledgements

* Brian Hunt, Logan Laszewski, Eliza Shane
* Dr. Su Dong, Faculty Advisor
