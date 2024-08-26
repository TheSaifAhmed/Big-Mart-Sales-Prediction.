# Big Mart Sales Prediction using XGBoost

This project aims to predict the sales of Big Mart stores based on historical sales data, using various predictive modeling techniques. The primary model used is XGBoost, a powerful gradient boosting algorithm known for its efficiency and performance.

## Project Overview

The Big Mart Sales Prediction project utilizes machine learning techniques to forecast sales based on various attributes such as store size, location, product type, and more. The goal is to provide accurate sales predictions that can help in inventory management, sales forecasting, and strategic decision-making.

## Features

  - **Data Preprocessing**: Handling missing values, encoding categorical variables, and feature scaling.
  - **Feature Engineering**: Creating new features that could potentially improve model accuracy.
  - **Model Training**: Using XGBoost, a robust and scalable machine learning algorithm.
  - **Regularization**: Implementing L1 (Lasso) and L2 (Ridge) regularization techniques to overcome overfitting and enhance model generalization.

## Model and Methodology

### Data Preprocessing

  - **Handling Missing Values**: Missing values in the dataset are handled using imputation techniques such as filling with mean, median, or mode.
  - **Categorical Encoding**: Categorical variables are encoded using one-hot encoding to make them suitable for the machine learning model.
  - **Feature Scaling**: Scaling features to ensure all are on a similar scale, which helps in faster convergence of gradient descent.

### Feature Engineering

New features were created based on domain knowledge and exploratory data analysis. These engineered features aim to capture underlying patterns that the basic features might not express.

### Model Training with XGBoost

The primary model used for this project is **XGBoost**, which is known for its speed and accuracy. It works by iteratively building decision trees and combining them to improve model performance.

### Regularization Techniques

To prevent the model from overfitting the training data, we implemented:

  - **L1 Regularization (`reg_alpha`)**: This technique adds a penalty proportional to the absolute value of the model coefficients. It helps in feature selection by driving less important feature weights to 
  zero, making the model simpler and more interpretable.
  - **L2 Regularization (`reg_lambda`)**: This technique adds a penalty proportional to the square of the model coefficients. It helps reduce model complexity and prevents the coefficients from becoming too 
  large, thereby reducing the model's variance.

By tuning these regularization parameters (`reg_alpha` and `reg_lambda`), we were able to achieve a balance between bias and variance, significantly reducing overfitting and improving the model's performance on unseen data, the regularization helped in reducing the R-Squared value between test and train data from 35% to 5% approx. .

## Results

The model has been evaluated on performance metrics i.e. R-Squared. With the implemented regularization techniques, the model generalizes well to new data, demonstrating reduced overfitting and improved predictive performance.
