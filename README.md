# Predicting Employee Attrition Using Logistic Regression

[![Python](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![Built with scikit-learn](https://img.shields.io/badge/Built%20with-scikit--learn-yellow.svg)](https://scikit-learn.org/)

> **Tagline**: *People Analytics in Action: From Attrition Risk to Retention Moves*

---

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Business Context](#business-context)
- [Data Description](#data-description)
- [Solution Approach](#solution-approach)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Modeling Pipeline](#modeling-pipeline)
- [Results](#results)
- [Key Insights](#key-insights)
- [Next Steps](#next-steps)

---

## Project Overview

This project demonstrates a complete **end-to-end machine learning pipeline** to predict employee attrition using a logistic regression classifier. It serves as a portfolio-ready case study showing applied data science in the HR domain, including data understanding, cleaning, feature engineering, modeling, evaluation, and interpretation of results.

---

## Problem Statement

McCurr Healthcare Consultancy, a global MNC, spends significant resources on retaining employees. Blanket incentives are costly, so their People Operations team asked for a **data-driven model** to identify which employees are at higher risk of leaving. This predictive model will help them target retention strategies more efficiently.

---

## Business Context

- Employees leaving an organization (attrition) cost time and money.
- HR needs to focus retention efforts where they matter most.
- This project demonstrates a way to estimate *attrition probability* and classify employee risk in a reproducible, explainable way.

---

## Data Description

The dataset includes **2940 employee records** with 33 features, such as:

- Demographics (Age, Gender, Education, Marital Status)
- Work characteristics (Job Role, Business Travel, OverTime)
- Satisfaction ratings (JobSatisfaction, EnvironmentSatisfaction, WorkLifeBalance)
- Performance (PerformanceRating, YearsSinceLastPromotion)
- Compensation (MonthlyIncome, PercentSalaryHike)
- The **target variable**: `Attrition` (Yes/No)

🔹 **Categorical Features**: 18  
🔹 **Numerical Features**: 15

There were **no missing values**, making this a clean HR dataset.

---

## Solution Approach

This project followed a standard, robust pipeline:

1. **Data Cleaning**  
   - Dropped constant or identifier columns (*EmployeeNumber, Over18, StandardHours*)  
   - Validated data types

2. **Feature Engineering**  
   - Encoded categorical variables using one-hot encoding  
   - Scaled continuous variables using z-score normalization

3. **Train-Test Split**  
   - 80/20 split for robust evaluation

4. **Modeling**  
   - Logistic Regression using scikit-learn  
   - Interpretable coefficients to communicate HR-relevant drivers

5. **Evaluation**  
   - Confusion Matrix  
   - Classification Report (Precision, Recall, F1-score)  
   - Precision–Recall curve to assess business trade-offs

---

## Exploratory Data Analysis

Some key EDA findings included:

- Average employee age: 37 years (range 18–60)  
- Median distance from home: 7 km  
- Salary: strongly right-skewed, median ~$6500  
- Most employees had a salary hike of ~15%  
- Average tenure: 7 years  
- Promotion frequency: on average every 2.2 years

Visuals included distribution plots, correlation heatmaps, and barplots to understand categorical feature frequencies.

---

## Modeling Pipeline

- Used `scikit-learn` logistic regression for its interpretability
- Created a repeatable pipeline for:
  - data transformation
  - model fitting
  - probability scoring
- Ensured reproducibility with random seeds
- Performance measured on test data for realistic generalization

---

## Results

- Logistic regression achieved balanced precision and recall  
- Class distribution (Attrition: 16%) handled with standard class weighting  
- Interpretable coefficients showed how key variables (e.g., OverTime, EnvironmentSatisfaction) influenced attrition risk  
- Confusion Matrix and PR curve showed reasonable performance for business use

---

## Key Insights

✅ Employees working overtime were at higher risk  
✅ Employees with poor environment or job satisfaction were more likely to leave  
✅ Long commute distance was another attrition driver  
✅ Employees with fewer recent promotions had higher attrition risk  
✅ The model is practical for quarterly HR reviews

---

## Next Steps

- Extend with advanced ensemble models (Random Forest, XGBoost)  
- Automate retraining in HR workflows  
- Build a Power BI or Tableau dashboard for HR teams  
- Integrate with an HRMS system for real-time scoring  

---
