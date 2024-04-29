# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
#### STEP 1 : Start
#### STEP 2 : Preprocessing the data
#### STEP 3 : Feature Extraction
#### STEP 4 : Training the SVM model
#### STEP 5 : Model Evalutaion
#### STEP 6 : Stop

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Meyyappan T
RegisterNumber:  2122232400864
*/


import pandas as pd
data = pd.read_csv("C:/Users/marco/OneDrive/Desktop/study materials/spam.csv",encoding = 'Windows-1252')
data

data.head()
data.tail()
data.isnull().sum()

x = data['v1'].values
y = data['v2'].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size= 0.2,random_state = 0)
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)
```

## Output:



### Using Count vectorizer and SVM:
![image](https://github.com/Meyyappan-T/Implementation-of-SVM-For-Spam-Mail-Detection/assets/128804366/2086fe50-a7f3-4d83-8762-b9674768b8bd)
### Accuracy:
![image](https://github.com/Meyyappan-T/Implementation-of-SVM-For-Spam-Mail-Detection/assets/128804366/f4505745-f782-48b3-90f0-7bcd6b1d5ff7)




## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
