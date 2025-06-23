# 🫀 Heart Failure Clinical Project: Predicting Ejection Fraction using Regression Analysis

This project explores the clinical dataset on heart failure patients to analyze factors affecting **ejection fraction** — a critical indicator of heart function. It applies **linear regression modeling** using R to predict ejection fraction based on biochemical and physiological attributes.

---

## 📁 Project Structure

This project includes:
- 📊 Exploratory Data Analysis (EDA)
- 📉 Correlation and statistical summaries
- 🧮 Multiple Linear Regression Modeling
- 📈 Model Diagnostics and Outlier Analysis
- 📦 Visualization using `ggplot2`, `corrplot`, `PerformanceAnalytics`, and more

---

## 📌 Dataset

- **Source**: [heart.csv](https://raw.githubusercontent.com/ABUALHUSSEIN/test/main/data/heart.csv)
- **Observations**: 299
- **Variables**: 13

| Feature                     | Description                                           |
|----------------------------|-------------------------------------------------------|
| `age`                      | Age of the patient (years)                            |
| `anaemia`                  | Anemia status (1 = yes, 0 = no)                       |
| `high_blood_pressure`      | Hypertension (1 = yes, 0 = no)                        |
| `creatinine_phosphokinase` | CPK enzyme level in blood (mcg/L)                     |
| `diabetes`                 | Diabetes status (1 = yes, 0 = no)                     |
| `ejection_fraction`        | % of blood leaving the heart per contraction          |
| `platelets`                | Platelet count (kiloplatelets/mL)                     |
| `sex`                      | Gender (1 = Male, 0 = Female)                         |
| `serum_creatinine`         | Serum creatinine level (mg/dL)                        |
| `serum_sodium`             | Serum sodium level (mEq/L)                            |
| `smoking`                  | Smoking status (1 = yes, 0 = no)                      |
| `time`                     | Follow-up time (days)                                 |
| `DEATH_EVENT`              | Death during follow-up (1 = yes, 0 = no)              |

---

## 📈 EDA Highlights

- Summary statistics and visualizations (histograms, boxplots)
- Joint plots and scatterplots using `WVPlots`
- Correlation heatmaps and scatter matrix visualizations
- Outlier detection using Cook's distance

---

## 📉 Model Summary

A multiple linear regression model was fitted with `ejection_fraction` as the dependent variable and the following predictors:

- `serum_sodium`
- `age`
- `platelets`
- `serum_creatinine`
- `time`
- `creatinine_phosphokinase`

### 🔍 Key Metrics

- Adjusted R²: ~0.025
- p-value: 0.03778
- Interpretation: Only `serum_sodium` showed statistical significance (p < 0.01)

---

## 🧪 Tools & Packages

```r
library(tidyverse)
library(caret)
library(ggcorrplot)
library(Metrics)
library(psych)
library(WVPlots)
library(PerformanceAnalytics)
library(car)
library(outliers)
