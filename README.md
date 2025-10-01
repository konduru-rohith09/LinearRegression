# LinearRegression

Linear Regression is a **supervised machine learning algorithm** used to predict a **continuous target variable** based on one or more features. It models the relationship between input features and the target using a linear equation.

---

## 1. Definition

Linear Regression predicts the target variable using a linear equation:

**Simple Linear Regression**:

\[y = \beta_0 + \beta_1 x + \epsilon\]

- `y`: Target variable  
- `x`: Feature variable  
- `β0`: Intercept  
- `β1`: Coefficient (slope)  
- `ε`: Error term  

**Multiple Linear Regression**:

\[y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_n x_n + \epsilon\]

---

## 2. Assumptions

- **Linearity:** Relationship between features and target is linear.  
- **Independence:** Observations are independent.  
- **Homoscedasticity:** Errors have constant variance.  
- **Normality:** Residuals are normally distributed.  
- **No Multicollinearity:** Features should not be highly correlated.  

---

## 3. Cost Function

Linear Regression uses **Mean Squared Error (MSE)**:

\[MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2\]

Goal: **Minimize MSE** to find the best-fitting line.



## 4. Optimization

- **Ordinary Least Squares (OLS):** Computes coefficients directly.  
- **Gradient Descent:** Iteratively updates coefficients to minimize error.  

---

## 5. Algorithm Steps

1. Initialize coefficients (`β0, β1, ...`)  
2. Compute predictions: `ŷi = β0 + Σ βj xij`  
3. Calculate error: `ei = yi - ŷi`  
4. Minimize error using OLS or Gradient Descent  
5. Repeat (if using Gradient Descent) until convergence  
6. Predict new data using final coefficients  
7. Evaluate performance using MSE, RMSE, and R²


## Evaluation Metrics
Mean Squared Error (MSE)
Root Mean Squared Error (RMSE)
Mean Absolute Error (MAE)
R² Score

##  Advantages
Simple and easy to understand
Fast training and prediction
Useful baseline for regression tasks
Provides insight into feature importance

## Limitations
Works only for linear relationships
Sensitive to outliers
Assumptions must hold true
Struggles with multicollinearity

## Real-Life Applications
Predicting house prices
Salary prediction based on experience
Sales forecasting
Stock market trend prediction
Medical research

## Visualization
Scatter plot shows actual data points.
Regression line shows predicted trend.
Helps visually check model fit.

## Summary
LinearRegression is a simple yet powerful algorithm for predicting continuous values. It is interpretable, computationally efficient, and ideal for baseline models or quick insights.

## Importing Libraries
The code uses:
pandas to create and handle the dataset.
matplotlib.pyplot to plot the data and regression line.
train_test_split to divide the dataset into training and testing sets.
LinearRegression to create and train the model.
mean_squared_error and r2_score to evaluate the model’s performance.

## Creating the Dataset
The dataset contains two columns:
Size → The area of the house (feature).
Price → The price of the house (target).
A pandas DataFrame is created with sample values for house sizes and prices.

## Defining Features and Target
X represents the feature(s), which is Size of the house.
y represents the target variable, which is Price.
X must be 2D, while y is 1D.

## Splitting the Dataset
The dataset is split into:
Training set → 80% of data, used to train the model.
Testing set → 20% of data, used to evaluate the model.
random_state ensures the split is reproducible.

## Training the Linear Regression Model
A Linear Regression model is created.
.fit() trains the model on the training data.

## During training, the model calculates:
Intercept → Base house price when size = 0.
Coefficient → How much the price increases per unit increase in size.

## Making Predictions
The trained model predicts house prices for the testing set.
Predictions are stored and compared with actual prices.

## Evaluating the Model
Intercept: Shows the base price of a house with size = 0.
Coefficient: Indicates price increase per unit of size.
Mean Squared Error (MSE): Measures average squared difference between predicted and actual prices.
R² Score: Measures how well the model explains price variation; closer to 1 is better.

## Key Takeaways:
Linear Regression fits a line that predicts house price from house size.
Intercept = starting price when size = 0.
Coefficient = price increase per unit of size.
Evaluation metrics like MSE and R² show model accuracy.
Visualization confirms how well predictions match actual prices
