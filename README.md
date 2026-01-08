# Early-Detection-of-FMD-in-cattle-Using-Machine-Learning

## Project Summary

This project focuses on the early detection of Bovine Foot and Mouth Disease (FMD) by applying machine learning and statistical modeling techniques to livestock field data.
Using R, the analysis identifies key risk factors associated with FMD infection and evaluates multiple classification models to support timely disease surveillance and control.

## Key Performance Indicators (KPIs)

1. FMD Prevalence Rate (%)
2. Model Accuracy
3. Sensitivity (Recall) – ability to correctly detect infected cattle
4. Specificity – ability to correctly identify non-infected cattle
5. F1 Score
6. Area Under the ROC Curve (AUC)
7. Top Predictive Risk Factors

## Dataset Overview

<a href="https://github.com/Lindamusundi47/Early-Detection-of-FMD-in-cattle-Using-Machine-Learning/blob/main/Raw%20data.xls"> Dataset </a>

Observations: 266 cattle samples
Target Variable: FMD_Status (Positive / Negative)
Predictor Variables:
1. Location: Districts, Kebeles
2. Animal factors: Breed, Sex, Age, Body Condition, Physiology
3. Environmental factors: Altitude, Agro-Climate

## Methodology

### 1. Data Cleaning & Preparation

- Renamed and standardized variables for consistency
- Verified no missing values or duplicates
- Converted categorical variables to factors
- Removed IDs and non-informative features

### 2. Handling Class Imbalance

- The original dataset was imbalanced (~80% Negative cases)
- I applied ROSE (combined over-sampling and under-sampling)
- Achieved a balanced dataset (~50:50) to improve model fairness and detection of positive cases

### 3. Exploratory Data Analysis (EDA)

-Generated stratified summaries by FMD status
-Examined distributions across demographic and environmental variables
-Performed correlation analysis to identify multicollinearity <a href="https://github.com/Lindamusundi47/Early-Detection-of-FMD-in-cattle-Using-Machine-Learning/commit/72ebd892db9ff2fd11e59cd1afaad9b073c50b55#diff-58b6beeb381aa0019466a1c17f2ebeda84deb6a171d5fcc1623644034a252a12"> Correlation Analysis </a>

### 4. Feature Selection

- Used the Boruta algorithm to identify statistically important predictors
- Reduced noise and improved model interpretability and performance

### 5. Modeling & Evaluation

- Split data into 70% training and 30% testing sets
- Trained and compared:
  1. Logistic Regression
  2. Random Forest
  3. Support Vector Machine (SVM)

-Evaluated models using confusion matrices, ROC curves, and classification metrics: <a href="https://github.com/Lindamusundi47/Early-Detection-of-FMD-in-cattle-Using-Machine-Learning/blob/main/Evaluation%20of%20models.png"> Evaluation of Models </a>

Random Forest achieved the best performance, making it the most suitable model for early detection of FMD in this dataset.

## Key Insights

-Poor body condition significantly increases the likelihood of FMD infection

-Older cattle showed higher infection rates

-Geographic location (Districts and Kebeles) strongly influenced disease prevalence

-Agro-climate and physiological status were consistent predictors across models
