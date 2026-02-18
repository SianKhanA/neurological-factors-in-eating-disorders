# Neurobehavioral Factors in Eating Disorders Prediction

## Project Overview
This project applies **Elastic Net Regression** with **Polynomial Features** to investigate the neurobehavioral drivers of eating disorders among university students in Bangladesh. The goal is to determine if demographic factors (Age, Gender, Region) can effectively predict a cumulative "Symptom Score" derived from behavioral survey data.

## The Dataset
The dataset consists of 550 observations and 57 features, categorized into:
* **Demographics:** Age Range, Gender, Division, etc.
* **Behaviors:** Frequency-based responses (Never to Often).
* **Body Perception:** Frequency of days (No days to Every day).

## Methodology
1. **Data Wrangling:** Converted ordinal text scales (e.g., "Sometimes", "Often") into numeric values (0-3).
2. **Feature Engineering:** Implemented `PolynomialFeatures` (degree=2) to capture interactions between demographic variables.
3. **Regularization:** Utilized `ElasticNetCV` to find the optimal balance between Lasso (L1) and Ridge (L2) penalties.

## Key Findings
* **Model Performance:** Achieved a Mean Absolute Error (MAE) of **7.28**.
* **$R^2$ Analysis:** The low $R^2$ score indicates that demographic factors alone are not strong predictors of eating disorder symptoms, suggesting that behavioral factors are more individualized.
* **Top Interaction Predictors:** * Interaction between `Bachelor's 4th Year` and `Marital_Status_Single`.
    * Regional variance, particularly in the `Khulna` division.

## Tools Used
* Python (Pandas, NumPy)
* Scikit-Learn (ElasticNetCV, PolynomialFeatures, StandardScaler)
* Matplotlib & Seaborn (Data Visualization)
