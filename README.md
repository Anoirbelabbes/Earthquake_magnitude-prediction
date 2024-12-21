# Earthquake Magnitude Prediction using Machine Learning

## Overview

This project focuses on predicting the magnitude of earthquakes using machine learning techniques. Predicting earthquake magnitude is a crucial task for disaster preparedness and mitigation efforts. This repository contains the code, data analysis, and model development for a system designed to estimate earthquake magnitudes based on various seismic features. We explore different regression models to identify the most effective approach for this predictive task.

## Problem Statement

Earthquakes are devastating natural disasters that cause significant loss of life and property damage. Accurate prediction of their magnitude can significantly improve early warning systems and inform better response strategies. This project aims to leverage machine learning to develop a robust and reliable model for earthquake magnitude prediction, moving beyond traditional statistical methods.

## Methodology

Our approach involved the following key steps:

1. **Data Acquisition and Exploration:**
   - We utilized a publicly available dataset of historical earthquake events, containing various physical and geographical measurements.
   - Exploratory Data Analysis (EDA) was performed to understand the data distribution, identify potential anomalies, and discover relationships between features. This included statistical analysis and visualizations.

2. **Data Preprocessing:**
   - **Handling Missing Values:** Strategies were implemented to address missing data points, such as imputation or removal, based on the nature and extent of missingness.
   - **Outlier Treatment:** Techniques like Winsorization were applied to mitigate the influence of extreme values in relevant features.
   - **Feature Engineering (Minimal in this version):** While not extensively explored here, potential future work could involve creating new features from existing ones.
   - **Data Transformation:**
     - **Normalization:** Numerical features were scaled to a uniform range (0 to 1) to ensure that no single feature unduly influences the models and to improve convergence speed.
     - **Log Transformation:** Applied to features with skewed distributions (e.g., number of stations) to reduce skewness and potentially improve model performance.
   - **Irrelevant Column Removal:**  Columns that were deemed non-predictive or redundant (like identifiers or highly granular location details) were removed to reduce noise and complexity.

3. **Model Development and Training:**
   - We experimented with several regression models to predict earthquake magnitude:
     - **Linear Regression:** A baseline model for establishing linear relationships between features and the target variable.
     - **Random Forest Regressor:** An ensemble learning method that combines multiple decision trees to improve prediction accuracy and robustness, capable of capturing non-linear relationships.
     - **Gradient Boosting Regressor:** Another powerful ensemble method that builds models sequentially, correcting errors from previous models, often achieving high predictive accuracy.
   - The dataset was split into training (80%) and testing (20%) sets to evaluate the generalization performance of the models.
   - Models were trained using the training data.

4. **Model Evaluation and Comparison:**
   - The performance of each model was evaluated on the testing dataset using appropriate regression metrics:
     - **R-squared (R²):**  Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables. A higher R² suggests a better fit.
     - **Root Mean Squared Error (RMSE):** Measures the average magnitude of the errors between predicted and actual values. A lower RMSE indicates better performance.
   - The performance metrics were compared to determine the most effective model for earthquake magnitude prediction.

5. **Model Selection:**
   - Based on the evaluation metrics, the **Gradient Boosting Regressor** emerged as the best-performing model for this task, demonstrating the highest R² and lowest RMSE on the test data.

## Getting Started

Follow these steps to run the code and replicate the results:

### Prerequisites

- **Python 3.x**
- **pip** (Python package installer)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Anoirbelabbes/Earthquake_magnitude-prediction.git
   cd Earthquake_magnitude-prediction
