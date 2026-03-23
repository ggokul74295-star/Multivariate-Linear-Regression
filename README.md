# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Step 1: Read the Dataset

Load the CSV file containing car data (Weight, Volume, CO2) into the system.

Step 2: Define Variables.

Select Weight and Volume as independent variables (inputs).

Select CO2 as the dependent variable (output).

Step 3: Create the Model

Initialize the Linear Regression model to establish a relationship between inputs and output.

Step 4: Train the Model

Fit the model using the dataset so that it learns the relationship between Weight, Volume, and CO2.

Step 5: Predict and Display Output

Provide new input values (Weight and Volume).

Predict the CO2 emission and display the coefficients, intercept, and predicted value.

## Program:
```
Developed By: Gokulan S
Register Number: 212225230078

import pandas as pd
from sklearn import linear_model

df = pd.read_csv("cars.csv")

x = df[['Weight', 'Volume']]
y = df['CO2']

regr = linear_model.LinearRegression()
regr.fit(x, y)

print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)

new_data = pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume'])
predictedCO2 = regr.predict(new_data)

print('Predicted CO2:', predictedCO2)

```
## Output:

<img width="853" height="457" alt="image" src="https://github.com/user-attachments/assets/389f9cd3-89f5-4c71-96fc-2bc6f18853ac" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
