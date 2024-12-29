# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 1.Import the standard Libraries.

2.Set variables for assigning dataset values.

3.Import linear regression from sklearn.

4.Assign the points for representing in the graph.

5.Predict the regression for marks by using the representation of the graph.

6.Compare the graphs and hence we obtained the linear regression for the given datas.

## Program:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error,mean_squared_error
df=pd.read_csv('student_scores.csv')
print(df)
df.head(0)
df.tail(0)
print(df.head())
print(df.tail())
x = df.iloc[:,:-1].values
print(x)
y = df.iloc[:,1].values
print(y)
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=1/3,random_state=0)
from sklearn.linear_model import LinearRegression
regressor = LinearRegression()
regressor.fit(x_train,y_train)
y_pred = regressor.predict(x_test)
print(y_pred)
print(y_test)
#Graph plot for training data
plt.scatter(x_train,y_train,color='black')
plt.plot(x_train,regressor.predict(x_train),color='blue')
plt.title("Hours vs Scores(Training set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
#Graph plot for test data
plt.scatter(x_test,y_test,color='black')
plt.plot(x_train,regressor.predict(x_train),color='red')
plt.title("Hours vs Scores(Testing set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
mse=mean_absolute_error(y_test,y_pred)
print('MSE = ',mse)
mae=mean_absolute_error(y_test,y_pred)
print('MAE = ',mae)
rmse=np.sqrt(mse)
print("RMSE= ",rmse)
```


## Output:
## Dataset

![image](https://github.com/user-attachments/assets/799d798b-e783-4ee3-9a03-e25af811aae4)

## Head Values
![image](https://github.com/user-attachments/assets/6d403087-2eb3-46a5-886f-4f7e815ae45a)


## Tail Values
![image](https://github.com/user-attachments/assets/e6ead08a-3a9d-4f98-b45d-67ac29f7a726)

## X and Y values
![image](https://github.com/user-attachments/assets/724acd1b-4137-4c6f-8713-b3e0be1f58b2)


## Predication values of X and Y
![image](https://github.com/user-attachments/assets/a12182eb-7d47-4ce5-be10-5d9db2bcb160)


## MSE,MAE and RMSE
![image](https://github.com/user-attachments/assets/ee1e9206-5cdb-4f6a-aabe-4014055d6196)


## Training Set
![image](https://github.com/user-attachments/assets/b9832442-921d-41e3-9c8c-1ca93b86e8a6)


## Testing Set
![image](https://github.com/user-attachments/assets/cd4fb883-cbf9-4949-913c-de7d7dde873f)

## Developed by : Gokul S
## Reg no: 24900980

## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.

