# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Step 1: Import the Pandas library and the required Linear Regression module from Scikit-learn.

Step 2: Load the carsemission.csv dataset into a Pandas DataFrame.

Step 3: Select Weight and Volume as independent variables and CO2 as the dependent variable.

Step 4: Create a Multivariate Linear Regression model and train it using the selected independent and dependent variables.

Step 5: Display the regression coefficients and intercept. Predict the CO₂ emission for a vehicle with Weight = 3300 and Volume = 1300.

## Program:
```
# Dataset Setup - Run this cell before starting the experiment

import pandas as pd

url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")
```
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:
<img width="1822" height="836" alt="Screenshot 2026-11-23 180924" src="https://github.com/user-attachments/assets/5e67ed68-3d4e-4d1d-b2a8-6d087539c1ad" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
