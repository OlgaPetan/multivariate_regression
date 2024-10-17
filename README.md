# multivariate_regression

This repository contains the code and analysis for a predictive modeling project. The goal of this project is to explore how different features affect a target variable, understand the relationships between the features, and assess different regression models for their effectiveness.

__Project Overview__
The project follows these main steps:

__1. Data Exploration and Health Check__
The first task is to examine the data to ensure it is clean and reliable:
  Check for missing values and outliers.
  Assess if any data corrections or adjustments are needed.
  Identify potential issues that may affect the analysis.

__2. Feature Analysis__
Next, I analyzed how each feature relates to the target variable:
  Investigated collinearity/multicollinearity between features.
  Considered feature selection and dimensionality reduction techniques.
  Explored the relationships between features and the target to identify which features may be most impactful.

__3. Predictive Modeling__
To test the predictive power of the features, I implemented the following models:
  __Recursive Feature Elimination (RFE):__ A feature selection model that ranks the most important features.
  __Multivariate Linear Regression:__ A standard linear regression model using all features.
  __Ridge Regression:__ Regularized regression to penalize large coefficients and reduce overfitting.
  __Lasso Regression:__ Similar to Ridge, but can set some coefficients to zero, effectively performing feature selection.
  __Polynomial Regression:__ Non-linear regression model to capture polynomial relationships between features.
  __XGBoost Regression Decision Tree:__ A powerful, tree-based ensemble method. I also tested a polynomial version and a reduced feature version based on the RFE results.

__4. Insights and Key Findings__
After testing the models, here are the general insights:
  No missing values or outliers were found in the data.
  No multicollinearity was detected between the features.
  Some features showed high variance and potential non-linear relationships with the target.
  Only 4 features had a somewhat positive correlation with the target variable.
  Dimensionality reduction was not feasible based on the available data.
  Ridge and Lasso regressions did not improve the R-squared compared to standard linear regression.
  The XGBoost regression tree significantly outperformed the linear models in terms of R-squared.
  Polynomial linear regression (degree=2) improved the R-squared for linear models but slightly reduced it for the XGBoost model.
  Recursive Feature Elimination (RFE) identified the same important features across all models.
  Using only the important features in a new XGBoost regression model slightly improved the R-squared, but given the lack of context for the features, it's uncertain if the rest of the features should be discarded.
