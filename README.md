# Physics-Informed Material Strength Prediction

Project Overview

This project aims to predict the compressive strength of concrete using a combination of machine learning techniques and physics-informed reasoning. By integrating domain knowledge from materials science and civil engineering, the model not only achieves high predictive accuracy but also provides actionable insights for engineers and decision-makers.

The objective is to demonstrate how physics-guided feature engineering can enhance traditional data-driven approaches, improving both model interpretability and reliability in real-world applications.

## Dataset Description

The dataset contains 1030 real-world concrete samples, capturing material compositions and curing parameters commonly used in construction and civil engineering projects.

Input Features:

Cement (kg/m³)

Blast Furnace Slag (kg/m³)

Fly Ash (kg/m³)

Water (kg/m³)

Superplasticizer (kg/m³)

Coarse Aggregate (kg/m³)

Fine Aggregate (kg/m³)

Age (days)

Target Variable:

Concrete Compressive Strength (MPa)

The dataset is clean, complete, and suitable for regression-based modeling.

## Methodology

The project follows a structured, physics-informed workflow:

Data Understanding and Inspection – Identify missing values, duplicates, and feature distributions.

Exploratory Data Analysis (EDA) – Examine relationships between mix components, curing age, and strength.

Physics-Informed Feature Analysis – Compute Water–Cement Ratio (WCR), Age × WCR interaction, and other features guided by concrete science.

Feature Engineering – Transform skewed variables, create interaction terms, and encode domain knowledge.

Model Training and Comparison – Evaluate linear models (OLS, Ridge, Lasso) and tree-based models (XGBoost).

Model Evaluation and Validation – Use RMSE, MAE, R², and cross-validation to ensure robustness.

Interpretability and Insights – Analyze feature importance, residuals, and identify optimal mix designs.

## Evaluation Metrics

Model performance is assessed using:

Root Mean Squared Error (RMSE)

Mean Absolute Error (MAE)

R² Score

Cross-validation R² to detect overfitting and ensure generalization

The XGBoost model achieved high R² (~0.95) and acceptable error rates, confirming its suitability for predicting concrete strength.

## Physics-Informed Insights

Key insights from the project that connect machine learning results to physical behavior include:

Water–Cement Ratio (WCR): Confirmed as the primary predictor of strength.

Age vs Strength: Non-linear growth — rapid early strength development, slower later.

Material Substitutions: Slag enhances strength at high cement content; fly ash had minimal effect in this dataset.

Feature Importance Analysis: Highlights which components most influence strength and where optimization efforts should focus.

Optimal Mix Design: Identified combinations of cement, slag, water, and superplasticizer that maximize predicted strength.

## Tools & Technologies

Programming Language: Python

Data Processing: NumPy, Pandas

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-learn, XGBoost

Statistical Analysis: SciPy

Environment: Jupyter Notebook / Google Colab

---
