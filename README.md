# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
#Ex 09 - Implementation of Decision Tree Regressor Model for Predicting the 
# Import libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.tree import DecisionTreeRegressor
# ------------------------------
# Step 1: Sample dataset
# ------------------------------
df = pd.read_csv('Salary.csv')
# ------------------------------
# Step 2: Split features and target
# ------------------------------
X = df[['Level']] # Feature (Level)
y = df['Salary'] # Target (Salary)
# ------------------------------
# Step 3: Create Decision Tree Regressor
# ------------------------------
regressor = DecisionTreeRegressor(random_state=42)
regressor.fit(X, y)
# ------------------------------
# Step 4: Predict salary for the dataset or new levels
# ------------------------------
y_pred = regressor.predict(X)
print("Predicted salaries:", y_pred)
# Example: predict salary for a new employee at level 6.5
level = np.array([[6.5]])
predicted_salary = regressor.predict(level)
print(f"Predicted Salary for level {level[0][0]}: {predicted_salary[0]}")
# ------------------------------
# Step 5: Visualize the results (High-resolution curve)
# ------------------------------
X_grid = np.arange(min(X.values), max(X.values)+0.01, 0.01) # High-resolut
X_grid = X_grid.reshape(-1, 1)
plt.scatter(X, y, color='red', label='Actual Salary')
plt.plot(X_grid, regressor.predict(X_grid), color='blue', label='Decision T
plt.title('Decision Tree Regression: Level vs Salary')
plt.xlabel('Level')
plt.ylabel('Salary')
plt.legend()
plt.show()
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: BRINDHA A R
RegisterNumber:  212225040050



## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
<img width="555" height="740" alt="Screenshot 2026-05-08 144754" src="https://github.com/user-attachments/assets/19dbef8d-f631-4aae-bae0-356cc4d0a9d8" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
