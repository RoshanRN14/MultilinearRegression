# Multilinear Regression

## Introduction
Linear regression is employed to forecast concrete compressive strength based on a dataset encompassing attributes like cement, water, aggregate, fly ash, and age, etc. This report delves into the application of linear regression in the context of predicting concrete strength and also verifying the assumptions of linear regression.

## Exploratory Data Analysis (EDA)
- Examined null and duplicate values. 25 duplicate rows were found and removed.
- Outliers present in various columns (Water, Superplasticizer, Age (day), Fine Aggregate, Blast Furnace Slag) were capped using IQR-based capping.
- Checked the normality of independent variables using QQ plots and KDE plots. Used box-cox transformation to transform the columns.

## Regression Assumptions and Results
- Analyzed the linear relationship of each independent variable with the dependent variable using Scatter Plots. Only the column 'Cement' shows a considerable linear relationship.
- Multicollinearity was checked by plotting a correlation heatmap and obtaining VIF scores of predictor columns. VIF scores came out to be in the acceptable range, indicating no perfect multicollinearity among independent variables.
- Mean of Residuals was calculated, and histplot of Residuals was plotted to check the normality. It came out to be more or less normal.
- Homoscedasticity was checked by plotting Residuals vs. Predicted Values Plot.

## Model Building
- Implemented linear regression as the predictive model due to its simplicity and interpretability.
- Divided the dataset into training and testing subsets.
- Trained the linear regression model using the training data.
- Applied Batch and Stochastic Gradient Descent algorithms.

## Model Evaluation
- Evaluated the model's performance on the testing data using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared Score.
- Assessed the model's goodness of fit and reliability in accurately predicting concrete compressive strength.

## Results
- The linear regression model demonstrated effectiveness in predicting concrete compressive strength.
- Using scikit-learn's LinearRegression:
  - MAE 0.32149806479575993
  - MSE 0.1673593239013553
  - R2 score 0.8336123056352251
- Using Gradient Descent:
  - R2 score 0.8336122006838834
- Using scikit-learn's SGDRegressor:
  - R2 score 0.8218532784047166
- Key predictors such as cement, water, and age significantly influenced the strength of concrete.
- Evaluation metrics indicated reasonable accuracy and precision in the predictions, validating the model's efficacy.
