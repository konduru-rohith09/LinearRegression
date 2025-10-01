Linear Regression - Machine Learning
🔹 Introduction

Linear Regression is one of the simplest and most widely used supervised machine learning algorithms. It is used to model the relationship between a dependent variable (target) and one or more independent variables (features) by fitting a straight line (in 2D) or a hyperplane (in higher dimensions).

It is mainly used for predicting continuous values such as house prices, sales, salary, etc.

🔹 How It Works

The model assumes a linear relationship between input features and the output variable:

𝑦
=
𝛽
0
+
𝛽
1
𝑥
1
+
𝛽
2
𝑥
2
+
⋯
+
𝛽
𝑛
𝑥
𝑛
+
𝜖
y=β
0
	​

+β
1
	​

x
1
	​

+β
2
	​

x
2
	​

+⋯+β
n
	​

x
n
	​

+ϵ

Where:

𝑦
y → Target variable (what we want to predict)

𝑥
1
,
𝑥
2
,
…
,
𝑥
𝑛
x
1
	​

,x
2
	​

,…,x
n
	​

 → Input features

𝛽
0
β
0
	​

 → Intercept (constant)

𝛽
1
,
𝛽
2
,
…
𝛽
𝑛
β
1
	​

,β
2
	​

,…β
n
	​

 → Coefficients (weights)

𝜖
ϵ → Error term

🔹 Types of Linear Regression

Simple Linear Regression → Uses one feature to predict the target.
Example: Predicting house price using only size.

Multiple Linear Regression → Uses multiple features.
Example: Predicting house price using size, location, and number of rooms.

🔹 Loss Function

The algorithm minimizes the Mean Squared Error (MSE):

𝑀
𝑆
𝐸
=
1
𝑛
∑
𝑖
=
1
𝑛
(
𝑦
𝑖
−
𝑦
^
𝑖
)
2
MSE=
n
1
	​

i=1
∑
n
	​

(y
i
	​

−
y
^
	​

i
	​

)
2
🔹 Assumptions of Linear Regression

Linearity → Relationship between X and y is linear.

Independence → Observations are independent of each other.

Homoscedasticity → Constant variance of residuals.

Normality of Errors → Errors are normally distributed.

No Multicollinearity → Independent variables should not be highly correlated.
