# Ex.No.1---Data-Preprocessing

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

##REQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

Kaggle :
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

Data Preprocessing:

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

Need of Data Preprocessing :

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:

1.Importing the libraries
2.Importing the dataset
3.Taking care of missing data
4.Encoding categorical data
5.Normalizing the data
6.Splitting the data into test and train

## PROGRAM:
```
Developed by: M.Pavithra
Reg no: 212222100032

import pandas as pd

df=pd.read_csv("/content/Churn_Modelling.csv")

df.head()

df.isnull().sum()

df.drop(["RowNumber","Age","Gender","Geography","Surname"],inplace=True,axis=1)

print(df)

x=df.iloc[:,:-1].values

y=df.iloc[:,-1].values

print(x)

print(y)

from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()

df1 = pd.DataFrame(scaler.fit_transform(df))

print(df1)

from sklearn.model_selection import train_test_split

xtrain,ytrain,xtest,ytest=train_test_split(x,y,test_size=0.2,random_state=2)

print(xtrain)

print(len(xtrain))

print(xtest)

print(len(xtest))

from sklearn.preprocessing import StandardScaler

sc = StandardScaler()

df1 = sc.fit_transform(df)

print(df1)
```
## OUTPUT:

## DATASET:

![exp1nn1](https://github.com/22008686/Ex.No.1---Data-Preprocessing/assets/118916413/6cba75fc-bbee-41d7-a696-8a58396017a6)

## VALUES OF INPUT AND OUTPUT DATA ON VAR X AND Y:

![exp 1nn2](https://github.com/22008686/Ex.No.1---Data-Preprocessing/assets/118916413/e6a4e663-5f26-4ecd-908e-98bc51152adf)

## NORMALISING DATA:

![exp1nn3](https://github.com/22008686/Ex.No.1---Data-Preprocessing/assets/118916413/0ff6bf11-d939-4a6d-a644-f66a9dfb2b6e)

## X AND Y TRAIN VALUES:

![exp1nn4](https://github.com/22008686/Ex.No.1---Data-Preprocessing/assets/118916413/8d0af872-c335-4aa7-b5a6-d08384c18bc8)

## X AND Y VALUES:

![exp1nn5](https://github.com/22008686/Ex.No.1---Data-Preprocessing/assets/118916413/44dae087-18e3-49a9-8d92-25a460752df7)

## X AND Y TEST VALUES:

![exp1nn6](https://github.com/22008686/Ex.No.1---Data-Preprocessing/assets/118916413/af9c159f-a081-42cf-b9f2-55ecd1ee0f26)

## RESULT:

Thus,the program to perform Data preprocessing in a data set downloaded from Kaggle is implemented successfully .
