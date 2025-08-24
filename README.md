# 📈 Sales Forecasting Project

This project demonstrates how to forecast future sales for a single product using historical monthly data. It walks through data preparation, applying multiple forecasting methods, evaluating their performance, and generating forecasts for future months.

## 📦 Packages Used
- pandas → For data loading, cleaning, and manipulation
- numpy → For numerical operations and array handling
- scikit-learn
    - LinearRegression → Builds a regression model to capture sales trends
    - mean_absolute_percentage_error → Evaluates model accuracy
- matplotlib → For creating visualizations and comparing actual vs. predicted sales
- warnings → Used to suppress unnecessary warnings during execution

## 🔄 Workflow Overview
1. Data Loading & Preparation
    - Load sales data from Sample_Data_Set.xlsx
    - Convert the Month column to datetime format and sort by product and month
    - Filter the dataset for a specific product (default: Product_3)

2. Train-Test Split
    - Split the product’s sales data into:
        - Training set: 75%
        - Testing set: 25%
    - Used to evaluate model forecasting accuracy

3. Forecasting Methods
    - Moving Average → Rolling window to predict future sales based on past averages
    - Linear Regression → Fits a regression model to capture trends in sales data
    - Quantile-Filtered Regression → Removes anomalies with the Interquartile Range (IQR) method before regression, improving robustness

4. Model Evaluation
    - Each method predicts sales for the test period
    - Accuracy is measured using Mean Absolute Percentage Error (MAPE)
    - The model with the lowest MAPE is selected as the best performer

## ✨ Key Features
- Multiple Forecasting Techniques → Compare simple and robust approaches
- Outlier Handling → Quantile filtering improves prediction accuracy
- Objective Model Selection → Based on MAPE evaluation
- Easy Customization → Swap out product names to forecast different items

## 🛠️ Core Functions

moving_average_forecast

linear_regression_forecast

quantile_filtered_forecast

Evaluation uses:

mean_absolute_percentage_error from scikit-learn
