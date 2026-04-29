# patient-no-show-analysis

## Overview
An end-to-end data science project analysing 106,975 medical appointment 
records to identify the key factors that influence whether patients show 
up for their appointments.

## Problem Statement
Medical no-shows cost healthcare systems millions annually. This project 
aims to identify the strongest predictors of no-show behaviour and build 
a predictive model to help hospitals reduce missed appointments.

## Dataset
- Source: Kaggle — Medical Appointment No Shows
- Size: 106,975 appointments
- Location: Brazil, 2016

## Key Findings
1. **Waiting time is the strongest predictor (57% importance)** — the longer 
   the gap between scheduling and appointment date, the higher the no-show risk
2. **Age is the second strongest predictor (38%)** — younger patients 
   (18-35) have the highest no-show rate at 24%
3. **SMS reminders paradoxically correlate with higher no-show rates** — 
   likely due to selection bias (high-risk patients targeted)
4. **Gender and health conditions have minimal predictive power**

## Model Results
| Model | No-show Recall | No-show F1 | Accuracy |
|-------|---------------|------------|---------|
| Logistic Regression | 1% | 0.03 | 80% |
| Random Forest (balanced) | 41% | 0.35 | 70% |

Random Forest with class balancing significantly outperforms Logistic 
Regression for this imbalanced dataset.

## Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (Logistic Regression, Random Forest)
- Jupyter Notebook

## Project Structure

patient-no-show-analysis/
│
├── patient_no_show_analysis.ipynb  # Main notebook
├── eda_visualisations.png          # EDA charts
├── feature_importance.png          # Feature importance chart
└── README.md

## Conclusions & Business Recommendations
- **Reduce scheduling gaps** — long waiting times are the biggest 
  driver of no-shows. Same-week appointments should be prioritised 
  where possible
- **Target younger patients** — implement stronger engagement strategies 
  for the 18-35 age group
- **Reconsider SMS strategy** — blanket SMS reminders are not effective. 
  Targeted reminders based on waiting time and age would be more impactful
