# EX 6 Implementation of Decision Tree Classifier Model for Predicting Employee Churn
## DATE:
## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import the employee churn dataset
2. if the dataset has missing values handel them using techiniques such as mean
3. convert categorical variables into numerical format using techniques such as noe_hot encoding
4. scale features if necessary using standardscaler


## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: chaithanya.c
RegisterNumber:  2305002004

import pandas as pd
from sklearn.tree import DecisionTreeClassifier,plot_tree
from sklearn.preprocessing import LabelEncoder
import matplotlib.pyplot as plt
df=pd.read_csv('/content/Employee_EX6.csv')
data = pd.read_csv('/content/Employee_EX6.csv')
data = df.copy()
data
le = LabelEncoder()
data['salary'] = le.fit_transform(data['salary'])
data
X = data.drop(['Departments','left'],axis=1)
Y = data['left']
clf = DecisionTreeClassifier()
clf.fit(X,Y)
plt.figure(figsize=(80,80))
plot_tree(clf, feature_names=X.columns,class_names=['LEFT','"NOT LEFT"'],filled=True,fontsize=14)
plt.show()
```

## Output:
![image](https://github.com/user-attachments/assets/2133d8c3-f79e-4ca8-842b-a14fe0355aaa)
![image](https://github.com/user-attachments/assets/d3d34e98-ef98-4ce1-ba27-b0a285076f65)
![image](https://github.com/user-attachments/assets/ffe2ecd4-be41-4094-b0e1-ad2c6add6301)
![image](https://github.com/user-attachments/assets/98f38d47-da20-4a34-914a-1623d55e2cf6)







## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
