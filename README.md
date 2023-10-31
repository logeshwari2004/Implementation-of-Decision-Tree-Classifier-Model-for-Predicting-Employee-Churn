# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas library to read csv or excel file.
2.Import LabelEncoder using sklearn.preprocessing library.
3.Transform the data's using LabelEncoder.
4.Import decision tree classifier from sklearn.tree library to predict the values.
5.Find accuracy.
6.Predict the values.
7.End of the program.

## Program:
```

Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:LOGESHWARI.P
RegisterNumber:212221230055  

```
```
import pandas as pd
data=pd.read_csv("Employee[1].csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
 from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()data["Departments "]=le.fit_transform(data["Departments "])
data.head(100)
data.info()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","Departments ","salary"]]
x.head()
x.info()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test= train_test_split(x,y,test_size=0.2,random_state=100)
x_train.shape

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2,1]])
```

## Output:
## data.head():
![277031420-c4bc31b2-79fc-41e4-ace3-09bb8948158f](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/080115ef-ab61-4972-9c79-df4f7e06fec8)
## data.info():
![277031633-b4df07f4-37e5-4efc-b5ae-7230d06b1e6e](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/884296ed-0343-40e4-a1e1-44bdd29ddbc7)
## data.isnull().sum()
![277031750-a03be87a-1e7a-4195-bc2f-42c76e900795](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/457e95bb-6f86-496a-b49f-1a52c46f0909)
![277031843-e48d1053-d4f6-4407-a6a5-7956aa9176a1](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/ba997360-2e5a-491e-a062-aad0336d04bd)


## After lable encoding:
![277032200-9ee8f9ef-7280-493c-a071-dfa64396660a](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/a5ff9b9c-6f09-4f0b-9333-0bb61c464fab)


## x_train.shape
![277032448-ae2ae673-738b-4939-917c-2a9709c38fae](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/5ec7357d-6213-4415-8dba-1847374d7ed9)


## y_pred
![277032703-be8a89c7-302d-451e-ae5d-d6460b5bfd41](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/c62c4820-b5e4-4b40-9dc2-cf865f73eb68)


## accuracy
![277032791-682ba873-1dde-47c3-8686-af5e1b957269](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/6e8aa9f9-50ee-4750-8d0c-5b823932ca3e)


## predicted value
![277032970-bbbfe749-ca6c-4c5a-a14e-b8d1551f209f](https://github.com/logeshwari2004/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/94211349/92211262-c9d6-4d71-9c37-4794228525d5)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
