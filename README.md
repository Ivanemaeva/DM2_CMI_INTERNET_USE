# Predicting Problematic Internet Use Severity — CMI Dataset

Data Mining 2 project (Università di Pisa, A.Y. 2025–2026) — Prof. Riccardo Guidotti.
Team: Fiza Naeem, Lorena Sorce, Ivane Maeva Nague.

## Overview

End-to-end pipeline on the Child Mind Institute (CMI) dataset, combining tabular and wearable-sensor time series data to predict problematic internet use severity in children/adolescents. Covers data understanding, outlier detection, classification, regression, time series analysis, and explainability (XAI).

## Methods & Results

**Data Understanding & Cleaning**
- 43 outliers identified and removed (tabular data)

**Classification**
- Best model: Macro F1 = 0.47 (XGBoost, with class imbalance handling)
- AdaBoost with 3-class setup, imbalanced learning techniques applied

**Regression**
- Best R² = 0.14 (severity score prediction)

**Time Series (actigraphy / accelerometer data)**
- Best classification accuracy on time series: 71%
- Shapelet-based classification, DTW-based hierarchical clustering, matrix profile / motif-discord discovery
- Statistical test on movement (anglez) regularity: p = 0.0006

**Explainability**
- LIME and SHAP applied to XGBoost and Random Forest models to interpret feature contributions

**Anomaly / Outlier Detection**
- KNN-based and HBOS anomaly detection on sensor data

## Repository structure


notebooks/
├── Module 0.ipynb                          # data understanding & prep
├── TimeSeries_Module0_prep.ipynb
├── xgb regressor + lime.ipynb
├── Module 2 xgb Classification + lime.ipynb
├── RF and SHAP.ipynb
├── un_inbalanced_classification.ipynb
├── Ada_boost with 3 classes.ipynb
├── TS_Classification_Clean.ipynb
├── TS_Shapelet_updated.ipynb
├── ShortTS-HIERARCHICAL-DTW.ipynb
├── MotifDiscord.ipynb
├── anomalyKNN.ipynb
├── hbos2.ipynb
├── Clustering final.ipynb
├── Real_DIFF METHODS_NeuralNetwork.ipynb
report/
└── DM2_report.pdf

## Tech stack

Python, pandas, scikit-learn, XGBoost, LIME, SHAP, sktime/tslearn (time series), imbalanced-learn

## Dataset

Child Mind Institute dataset — tabular questionnaire data + wrist-worn accelerometer time series.

## Voto
30/30
