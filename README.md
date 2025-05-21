# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.import pandas module and import the required data set.
2.Find the null values and count them. 
3.Count number of left values.
4.From sklearn import LabelEncoder to convert string values to numerical values.
5.From sklearn.model_selection import train_test_split.
6.Assign the train dataset and test dataset.
7.From sklearn.tree import DecisionTreeClassifier.
8.Use criteria as entropy.
9.From sklearn import metrics.
10.Find the accuracy of our model and predict the require values.
```
## Program:
```.py
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: THIRUMURUGAN R
RegisterNumber: 212223221008
*/

  import pandas as pd
  data=pd.read_csv("Employee.csv")
  data.head(5)
  data.isnull().sum()
  data["left"].value_counts()
  from sklearn.preprocessing import LabelEncoder
  le=LabelEncoder()
  data["salary"]=le.fit_transform(data["salary"])
  data.head()
  x=data[["satisfaction_level","last_evaluation","Work_accident","promotion_last_5years","number_project","average_montly_hours","time_spend_company","salary"]]
  x.head()
  y=data["left"]
  y.head()
  from sklearn.model_selection import train_test_split
  x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
  from sklearn.tree import DecisionTreeClassifier
  dt=DecisionTreeClassifier(criterion="entropy")
  dt.fit(x_train,y_train)
  y_pred=dt.predict(x_test)
  y_pred
  from sklearn import metrics
  accuracy=metrics.accuracy_score(y_test,y_pred)
  accuracydt.predict([[0.5,0.8,9,260,6,0,1,2]])


```

## Output:

## DATA HEAT

![Screenshot 2025-04-10 203412](https://github.com/user-attachments/assets/2b73d3b9-cfbe-4c00-a911-ea54f3bf6786)
## DATASET INFO

![image](https://github.com/user-attachments/assets/950cc693-663a-4358-89e2-dc7517bc5cb5)
##        NULL DATASET
##        VALUES COUNT IN LEFT COLUMN:

![Screenshot 2025-04-10 204430](https://github.com/user-attachments/assets/d251ce78-630a-4dd1-9eeb-c7172293ad45)
## DATASET TRANSFORMED HEAD:

![Screenshot 2025-04-10 203708](https://github.com/user-attachments/assets/fd0623fc-126f-4b3a-8f13-ff90fbaf0488)
## X.HEAD:

![image](https://github.com/user-attachments/assets/a3aa98ec-9e02-4e1f-99fa-f398bb8acf86)
## ACCURACY:

![image](https://github.com/user-attachments/assets/35d9d737-d083-4d24-85d5-e261c93d44ca)


## DATA PRIDECTION:
![Screenshot 2025-04-10 203800](https://github.com/user-attachments/assets/22a8ceb9-3840-4fc0-8d6e-203bd477db75)




## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
