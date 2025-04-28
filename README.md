<H3>POPURI SRAVANI</H3>
<H3>212223240117</H3>
<H3>EX. NO.1</H3>
<H3>26.04.2025</H3>
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
# import libraries
```
import pandas as pd 
import seaborn as sns 
import StandardScaler from sklearn.preprocessing 
import MinMaxScaler from sklearn.model_selection
import train_test_split from scipy 
import stats
import numpy as np
```
# Read the dataset
```
df=pd.read_csv("Churn_Modelling.csv") df.head() df.tail() df.columns
```
# Check the missing data
```
df.isnull().sum() df.duplicated()
```
# assigning y
```
y = df.iloc[:, -1].values print(y)
#check for duplicates
df.duplicated()
```

# check for outliers
```
df.describe()
droping string values data from dataset
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
```

# Checking datasets after dropping string values data from dataset
```
data.head()
```

# Normalize the dataset
```
scaler=MinMaxScaler() df1=pd.DataFrame(scaler.fit_transform(data)) print(df1)
```

# Split the dataset
```
X=df.iloc[:,:-1].values y=df.iloc[:,-1].values print(X) print(y)
```

# Training and testing model
```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2) print("X_train\n") print(X_train) print("\nLenght of X_train ",len(X_train)) print("\nX_test\n") print(X_test) print("\nLenght of X_test ",len(X_test))
```




## OUTPUT:
# Data checking
![Screenshot 2025-04-28 081658](https://github.com/user-attachments/assets/dac30779-c998-4c50-b92c-775decceecd0)
# Duplicates Identification
![Screenshot 2025-04-28 081728](https://github.com/user-attachments/assets/a50d238d-08e2-44c8-acda-c6733b667f85)
# Values of y
![Screenshot 2025-04-28 081737](https://github.com/user-attachments/assets/0b0ffdf2-3dc5-47f0-a024-04fa0e904dbc)
# Outliers
![Screenshot 2025-04-28 081815](https://github.com/user-attachments/assets/d1f5ef45-4bed-412e-977b-3f2ec35bf767)
# Checking datasets after dropping string values data from dataset
![Screenshot 2025-04-28 081800](https://github.com/user-attachments/assets/e62ebaf3-4f6e-4741-9029-35e40c83329b)
# Normalize the dataset
![Screenshot 2025-04-28 081838](https://github.com/user-attachments/assets/c98b0792-8f08-4ff8-b268-8cf3ec773082)
# Split the dataset
![Screenshot 2025-04-28 081847](https://github.com/user-attachments/assets/06cf65fd-5af1-4f24-bc7b-75474fcdcc3b)
# Training the model
![Screenshot 2025-04-28 081855](https://github.com/user-attachments/assets/e9ac19a9-4c92-4209-af8f-04cc035ff040)
# Testing the model
![Screenshot 2025-04-28 081903](https://github.com/user-attachments/assets/1f0175d4-4c44-4896-93d3-ae915c0a639a)






## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


