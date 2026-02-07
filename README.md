# Physics-Informed Material Strength Prediction

## Project Overview
This project predicts the **compressive strength of concrete** using a combination of **machine learning** and **physics-informed reasoning**. By integrating domain knowledge from **materials science and civil engineering**, the model achieves high predictive accuracy while providing actionable insights for engineers and decision-makers.  

The goal is to demonstrate how **physics-guided feature engineering** can improve traditional data-driven approaches, enhancing both **interpretability** and **reliability**.

---

## Dataset Description
The dataset contains **1030 real-world concrete samples** capturing material composition and curing parameters used in construction.  

**Input Features:**

- Cement (kg/m³)  
- Blast Furnace Slag (kg/m³)  
- Fly Ash (kg/m³)  
- Water (kg/m³)  
- Superplasticizer (kg/m³)  
- Coarse Aggregate (kg/m³)  
- Fine Aggregate (kg/m³)  
- Age (days)  

**Target Variable:**

- Concrete Compressive Strength (MPa)  

---

## Methodology
The workflow of the project includes:

1. **Data Understanding and Inspection** – Check for missing values, duplicates, and feature distributions.  
2. **Exploratory Data Analysis (EDA)** – Analyze relationships between mix components, curing age, and strength.  
3. **Physics-Informed Feature Engineering** – Create Water–Cement Ratio (WCR), Age × WCR, and other domain-driven features.    
4. **Model Evaluation and Validation** – Use RMSE, MAE, R², and cross-validation to ensure robustness.  
5. **Interpretability and Insights** – Analyze feature importance, residuals, and identify optimal mix designs.
6. **Deploying Model** - Attaching model with DataBricks SQL Warehouse.

---

## Evaluation Metrics
Model performance was assessed using:

- **Root Mean Squared Error (RMSE)**  
- **Mean Absolute Error (MAE)**  
- **R² Score**  
- **Cross-validation R²** for overfitting detection  

The XGBoost model achieved **R² ≈ 0.95**, confirming high predictive accuracy.

---

## Physics-Informed Insights
Key findings connecting ML results to concrete physics:

- **Water–Cement Ratio (WCR)**: Main predictor of strength.  
- **Age vs Strength**: Non-linear growth; rapid early strength gain slows over time.  
- **Material Substitutions**: Slag improves strength; Fly ash had minimal effect in this dataset.  
- **Feature Importance**: Identifies components that most affect strength.  
- **Optimal Mix Design**: Cement, slag, water, and superplasticizer ratios maximizing predicted strength.

---

## Best Mix Design (Predicted Strength)

| Component / Parameter        | Value | Unit       |
|-------------------------------|-------|------------|
| Cement                        | 390   | kg/m³      |
| Blast Furnace Slag            | 189   | kg/m³      |
| Fly Ash                        | 0     | kg/m³      |
| Water                         | 146   | kg/m³      |
| Superplasticizer              | 22    | kg/m³      |
| Coarse Aggregate              | 945   | kg/m³      |
| Fine Aggregate                | 756   | kg/m³      |
| Curing Age                    | 91    | days       |

