# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM :

To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required :

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm :

### Step 1 :

Import the necessary python packages using import statements.

### Step 2 :

Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

### Step 3 :

Split the dataset using train_test_split.

### Step 4 :

Calculate Y_Pred and accuracy.

### Step 5 :

Print all the outputs.

### Step 6 :

End the Program.

## Program :

### Program to implement the SVM For Spam Mail Detection.
### DEVELOPED BY : Gumma Dileep Kumar
### REG NO : 212222240032

```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')

data.head()

data.info()

data.isnull().sum()

x=data["EmailText"].values
y=data["Label"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extractiaon.text import CountVectorizer
cv=CountVectorizer()

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
```

## Output :

### DATA.HEAD() :


![ml_9 1](https://github.com/gummadileepkumar/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118707761/ac77444b-1022-425d-b303-efa7e3d5c79e)


### DATA.INFO() :


![ml_9 2](https://github.com/gummadileepkumar/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118707761/2e0d912a-833d-4985-b62e-d6d99a661d35)



### DATA.ISNULL().SUM() :


![ml_9 3](https://github.com/gummadileepkumar/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118707761/fb5447f6-dcc6-41da-8221-d6e65b39d451)


### Y_PRED :

![ml_9 4](https://github.com/gummadileepkumar/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118707761/d9efe245-7ab3-4646-a72d-afc40a882cc5)




### ACCURACY :


![ml_9 5](https://github.com/gummadileepkumar/Implementation-of-SVM-For-Spam-Mail-Detection/assets/118707761/95fdc0a2-f1a2-43eb-aff5-5d0167e77bd5)



## Result :

Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
