# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required packages. 
2.Read the data set. 
3.Apply label encoder to the non-numerical column inoreder to convert into numerical values. 
4.Determine training and test data set. 
5.Apply decision tree regression on to the dataframe and get the values of Mean square error, r2 and data prediction.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by  : NIRAUNJANA GAYATHRI G R
RegisterNumber:  22008369

import pandas as pd
data=pd.read_csv("Salary.csv")
print("data.head")
data.head()

print("data.info")
data.info()

print("isnull    sum")
data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
print("data.head() for salary")
data.head()

x=data[["Position","Level"]]
y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
print("MSE value")
mse

r2=metrics.r2_score(y_test,y_pred)
print("r2 value")
r2

print("data prediction")
dt.predict([[5,6]])
*/
```

## Output:
![image](https://github.com/niraunjana/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119395610/864f5ce8-7edf-47ce-a8d3-69f0ef550c2c)

![image](https://github.com/niraunjana/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119395610/6eb681a2-8f3b-4b6f-ace5-7b2b46fe3474)

![image](https://github.com/niraunjana/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119395610/ea4b8bc1-145f-4c19-a220-1b67ca98f1c6)

![image](https://github.com/niraunjana/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119395610/aae5b83a-8194-4083-8e0e-38f2f4392914)

![image](https://github.com/niraunjana/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119395610/26f6b47c-f8c3-4b25-8864-6dd166d7d565)

![image](https://github.com/niraunjana/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119395610/d23a7b9a-2e06-4fbc-b4a6-8ff66c53946a)

![image](https://github.com/niraunjana/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119395610/fff7a141-5a4f-4c51-bc8e-ec1d21e23fc6)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
