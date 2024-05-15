# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the necessary packages.

2.Read the given csv file and display the few contents of the data.Assign the features for x and y respectively.

3.Split the x and y sets into train and test sets.Convert the Alphabetical data to numeric using CountVectorizer.

4.Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.

5.Find the accuracy of the model.

## Program:

```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: PYNAM VINODH
RegisterNumber: 212223240131

import chardet
file = '/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data= pd.read_csv("/content/spam.csv",encoding='Windows-1252')

data.head()

data.info()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:

# Result Output:

![image](https://github.com/PYNAMVINODH/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742678/51ad2e4c-3626-4861-86b0-67279e324735)


# data.head()

![image](https://github.com/PYNAMVINODH/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742678/c6f5e650-be0a-45a1-b34d-63c27ebb9397)


# data.info()

![image](https://github.com/PYNAMVINODH/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742678/686e672d-f2be-4564-8080-8930f8a02a9b)


# data.isnull().sum()

![image](https://github.com/PYNAMVINODH/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742678/e8624225-f939-404b-aea8-2aee60569f3e)


# Y_Prediction value

![image](https://github.com/PYNAMVINODH/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742678/6972bd85-da87-439e-ba52-08dd8fa2de7a)

# Accuracy Value

![image](https://github.com/PYNAMVINODH/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742678/8b4f6484-1625-4a30-8d2f-88e795c7cb72)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
