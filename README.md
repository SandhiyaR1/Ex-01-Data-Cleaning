# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUPUT
### DATA:
![d1](https://user-images.githubusercontent.com/113497571/226186745-eabbd740-57e6-43a4-8606-c6b040c781d0.jpg)
# NON NULL BEFORE:

### df.info:
![d2](https://user-images.githubusercontent.com/113497571/226186796-ca173f52-8a09-458b-8975-e672fdcb8fa7.jpg)
### MODE:
![modeee](https://user-images.githubusercontent.com/113497571/226186860-388cd405-bd54-4df2-8b59-bebc581153b9.jpg)
### MEAN:
![MEAN](https://user-images.githubusercontent.com/113497571/226186937-eaac0650-9496-40b1-8a50-fe84f9fc6a72.jpg)
### MEDIAN:
![median](https://user-images.githubusercontent.com/113497571/226187045-91e73265-6b9d-4d53-9c7e-a06c86bfe710.jpg)
# NON NULL AFTER:
### df.info:
![df info after](https://user-images.githubusercontent.com/113497571/226187111-880de989-24ef-4394-b1bd-d259c7a23644.jpg)
### df.isnull().sum():
![dh isnull() ](https://user-images.githubusercontent.com/113497571/226527636-244b2fc4-6447-44d6-8d98-81be75169133.jpg)

# RESULT:
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
