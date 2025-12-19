# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:

Step 1: Start

Begin the process.

Step 2: Input the Dataset



Let X = {x₁, x₂, x₃, …, xₙ} be the independent variables (features)

Let y be the dependent (target) variable


Step 3: Preprocess the Data


Add a column of ones to X for the bias (intercept) term


Step 4: Initialize Parameters

Initialize the parameter vector θ = {θ₀, θ₁, θ₂, …, θₙ} with zeros or small random values



Step 5: Hypothesis Function

Compute the predicted output using:

h_\theta(X) = θ₀ + θ₁x₁ + θ₂x₂ + … + θₙx

## Program:
```


import pandas as pd
from sklearn import linear_model
df = pd.read_csv("car.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
predictedCO2 = regr.predict(pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume']))
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)



```
## Output:
![WhatsApp Image 2025-12-19 at 8 58 42 PM (1)](https://github.com/user-attachments/assets/e0f3eef3-d3e5-4dba-9a61-18756ff0db57)

### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
