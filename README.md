<H3>PRAVIN KUMAR A</H3>
<H3>20222323015</H3>
<H3>EX. NO.1</H3>
<H3>03.03.24</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

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
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
data=pd.read_csv("/kaggle-raw.csv")
data

# spliting the dataset
X = data.iloc[:, :-1].values
print(X)

# finding the missing values
data.isnull().sum()


# Handling the missing values
data.fillna(data.mean().round(1), inplace=True)
data


data.isnull().sum()
data


y=data.iloc[:, -1]
print(y)


# check for duplication
data.duplicated()
data

# Outlier detections
print(data["Author_name"].describe)

# spliting the dataset for training & testing
X_train,X_test,y_train,y_test=train_test_split(X,y,test_size=0.2)
print(X_train)
print(len(X_train))
print(X_test)
print(len(X_test))

## OUTPUT:
# READ CSV FILE
![read](https://github.com/RAVENPRAVIN/Ex-1-NN/assets/146820534/d2131384-e9f2-4ce6-8b4e-9564f123b3cb)

# NULL VALUE
![null value](https://github.com/RAVENPRAVIN/Ex-1-NN/assets/146820534/e38c9dc4-a784-4b74-bb28-715725124316)

# Handling the missing values
![haling](https://github.com/RAVENPRAVIN/Ex-1-NN/assets/146820534/18a092c4-f874-46c1-b318-d19c2cc2c522)

# DUPLICATION
![duplication](https://github.com/RAVENPRAVIN/Ex-1-NN/assets/146820534/a0461eb2-26c6-489d-9ce6-157086cdffea)

# SPLIT
![spliting](https://github.com/RAVENPRAVIN/Ex-1-NN/assets/146820534/b72d0798-c5c3-4489-b7d0-6a4176203937)
### 
![y](https://github.com/RAVENPRAVIN/Ex-1-NN/assets/146820534/b7c2d8ac-d0dc-4d0b-8f56-86a47278bac5)

# OUTLIER AND DETECTION

![outliers and detection](https://github.com/RAVENPRAVIN/Ex-1-NN/assets/146820534/56cdcd5b-0291-4de7-bb3c-3a9203ee5d62)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


