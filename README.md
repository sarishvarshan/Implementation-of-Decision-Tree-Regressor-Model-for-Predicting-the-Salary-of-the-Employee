# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee 

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries. 
2. Upload the csv file and read the dataset. 
3. Check for any null values using the isnull() function.
4. From sklearn.tree inport DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Sarish Varshan V
RegisterNumber:  212223230196
*/
```
```
import pandas as pd
data=pd.read_csv("C:\Users\giri9\Downloads\Salary.csv")
data.head()
```
```
data.info()
```
```
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['Position']=le.fit_transform(data['Position'])
data.head()
```
```
x=data[['Position','Level']]
y=data['Salary']
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_predict)
mse
```
```
r2=metrics.r2_score(y_test,y_predict)
r2
```
```
dt.predict([[5,6]])
```


## Output:
### df.head()
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/152167665/c12c257c-aa79-4f61-8080-20dfdfbe2fc6)
### df.info()
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/152167665/6f592a33-f577-4e1c-917a-3fea7f5c0bac)
### data.isnull().sum()
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/152167665/bd5f18c8-5d22-49ea-b1c2-9c9e1148b6c1)
### data.head()for position
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/152167665/bf06b81b-dee7-45a1-bf84-80e2490d53a5)
### MSE value
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/152167665/c152a51e-e4ae-44cd-b53e-d980fd435772)
### R2 value
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/152167665/70bd8fe4-ba3b-4e3c-9e6f-564210bbbbe4)
### Prediction value
![image](https://github.com/sarishvarshan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/152167665/271c7d35-79e1-4ecb-a181-fe92cc5a0dd5)











## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
