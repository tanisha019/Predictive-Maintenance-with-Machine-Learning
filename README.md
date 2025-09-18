# Predictive Maintenance using Machine Learning

## Project Overview
This project demonstrates how machine learning can be applied to predictive maintenance tasks — identifying machine components that are likely to fail before breakdown occurs.  
By analyzing telemetry data, error logs, maintenance history, and machine metadata, the model predicts which component is most likely to fail.  

This type of solution is critical in industries such as manufacturing, mining, and energy, where unplanned downtime can cause significant financial losses.

---

## Key Objectives
- Predict which component of a machine is likely to fail.  
- Reduce unplanned downtime by enabling proactive maintenance.  
- Build an end-to-end ML pipeline: data preparation → feature engineering → modeling → evaluation.  
- Demonstrate the importance of feature engineering in time-series and maintenance problems.  

---

## Dataset
The dataset is a publicly available simulated predictive maintenance dataset inspired by Microsoft’s case study.

It includes:
- Telemetry: Voltage, rotation, pressure, vibration (hourly sensor data).  
- Error Logs: Non-fatal error codes recorded per machine.  
- Maintenance Records: Component replacements and inspection logs.  
- Failure History: Labels of actual component failures.  
- Machine Metadata: Machine model, age, and ID.  

Reference or download instructions can be added if the dataset is not included directly in this repository.

---

## Project Workflow
1. Data Preprocessing  
   - Cleaned and merged multiple datasets (telemetry, errors, maintenance, failures, metadata).  
   - Handled missing values and aligned timestamps.  

2. Feature Engineering  
   - Created lag features (3h, 24h moving averages for telemetry).  
   - Aggregated error counts over time windows.  
   - Computed "time since last component replacement".  
   - Incorporated machine age and model type as predictors.  

3. Exploratory Data Analysis (EDA)  
   - Visualized telemetry trends and error distributions.  
   - Identified correlations between machine health and failures.  

4. Model Development  
   - Baseline models: Logistic Regression, Random Forest.  
   - Compared model performance using confusion matrix, precision, recall, and F1-score.  
   - Addressed class imbalance by evaluating per-class performance.  

5. Model Explainability  
   - Used feature importance analysis to understand key drivers of failures.  
   - Suggested SHAP/LIME for interpretability (future extension).  

---

## Results
- Achieved accurate classification of machine failures across multiple components.  
- Random Forest performed better than baseline Logistic Regression.  
- Feature engineering (rolling averages, time since last replacement) significantly improved predictive power.  

Example Results:
- Confusion Matrix (per component failure).  
- Feature Importance Plot.  
- Precision-Recall Analysis for rare failure events.  

---

## Business Impact
- Enables early detection of failures, reducing downtime.  
- Supports cost-effective maintenance scheduling.  
- Demonstrates how combining multiple data sources (telemetry, logs, maintenance) improves predictions.  

---
