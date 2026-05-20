# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.Import the required libraries pandas and linear_model from sklearn.

2.Read the dataset car.csv using pd.read_csv().

3.Select Weight and Volume as input variables (X) and CO2 as output variable (y).

4.Create the Linear Regression model using linear_model.LinearRegression().

5.Train the model using regr.fit(X, y).

6.Display the coefficients and intercept of the regression model.

7.Predict the CO2 emission for the given values of Weight = 3300 and Volume = 1300 using predict().

8.Display the predicted CO2 value.

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


<img width="957" height="332" alt="image" src="https://github.com/user-attachments/assets/b4cfbb9e-0c20-49ed-a3a4-b4918511301c" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
