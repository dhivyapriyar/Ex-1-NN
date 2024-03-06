## ENTER YOUR NAME : Dhivyapriya.R
## ENTER YOUR REGISTER NO.: 212222230032
## DATE:
## EX 1 Introduction to Kaggle and Data preprocessing

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:

STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```
```
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df
```
```
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df
```
```
df.isnull().sum()
```
```
df.duplicated()
```
```
df.describe()
```
```
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1
```
```
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y
```
```
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```


## OUTPUT:

## DATASET

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/dc1505ff-5402-4a6f-88d0-2416dd58f3f0)


## DROPPING THE UNWANTED DATASET

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/bfd95e92-de13-47aa-9eff-663608fdb9e6)


## CHECKING NULL VALUES

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/10fcb0c0-ef17-4e31-8e99-2dfc5284bcac)

## CHECKING FOR DUPLICATION

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/a5f478cb-0064-45b7-bf46-4c171946892a)


## DESCRIBING THE DATASET

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/0f3bf402-cda6-4ecb-8ae3-41d5a94f224a)


## SCALING THE DATASET

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/d59f09e6-4598-40d1-8363-343dd07cf6e8)

## X FEATURES

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/acddd8ba-ab86-43ac-bf27-61f2dd813bb0)


## Y FEATURES

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/00b0f4a5-dd35-4510-aa26-319a1a5a208c)

## SPLITTING THE TRAINING AND TESTING DATASET:

![image](https://github.com/dhivyapriyar/Ex-1-NN/assets/119477552/6f97cac3-8313-4c9c-aa3e-c039b0a0c8b5)

## RESULT:

Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


