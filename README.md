# Predictive Maintenance Using Machine Learning

## Project Overview
This project develops a machine learning-based predictive maintenance system aimed at forecasting equipment failures in industrial machinery. Using multi-source data including sensor telemetry, error logs, maintenance records, and machine information, it predicts the likelihood of component failures to reduce downtime and optimize maintenance schedules.

## Data Sources
- **Telemetry Data:** Time-series sensor measurements such as voltage, rotation, pressure, and vibration collected hourly from multiple machines.
- **Error Logs:** Non-breaking error records captured over time, providing insights into machine anomalies.
- **Maintenance Records:** Scheduled and unscheduled component replacements, including failure events.
- **Machine Profiles:** Metadata about each machine including model type and years in service.

## Project Workflow

### 1. Data Collection and Integration
Combine heterogeneous datasets collected from different sources by timestamp and machine ID to create a unified dataset suitable for analysis.

### 2. Feature Engineering
- Generate lag features and rolling statistics (mean, standard deviation) from sensor telemetry to capture short- and long-term operational trends.
- Count error occurrences over lagging time windows to identify recurring issues.
- Calculate days since last component replacement from maintenance logs as a key predictive feature.
- Incorporate static machine characteristics such as model and age.

### 3. Data Preprocessing
- Handle missing values and align data granularity.
- Normalize and scale features as needed for modeling.

### 4. Model Building
- Formulate the problem as a multi-class classification task to predict which component might fail.
- Train multiple machine learning algorithms (e.g., logistic regression, random forest, XGBoost) on the engineered features.
- Fine-tune hyperparameters using cross-validation for optimal performance.

### 5. Model Evaluation
- Evaluate models using metrics suited for imbalanced data: precision, recall, F1-score, ROC-AUC.
- Select the best-performing model based on predictive accuracy and business impact.

### 6. Insights and Impact
- The predictive model supports proactive maintenance decisions, minimizing unplanned downtime.
- Demonstrates the value of integrating diverse data sources and domain-specific feature engineering in industrial applications.
