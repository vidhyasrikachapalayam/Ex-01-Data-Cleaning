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
import pandas as pd

df=pd.read_csv("/content/Loan_data.csv")

print(df)

df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])

df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])

df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())

df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())

df.head()



df.info()

df.isnull().sum()

# OUPUT
DATA:

![1](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/555271ae-eeec-49d7-9a5b-32b58968cd75)


![01](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/dbc571f0-b88c-4356-abc5-46ee0589ccd4)


NON NULL BEFORE:

![2](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/6f57a81f-6651-413b-8a3d-f1cbf0dc6377)

![02](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/3b6085b9-6dda-482f-8200-e065e5ba4c0b)

MODE:

![3](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/59ac840c-741c-4ccf-933b-c06cdbfc625a)

MEAN:

![4](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/5e229c13-cd15-4965-a9f6-7646d27e924d)

MEDIAN:

![6](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/de44515c-2f91-4dda-9397-61741734403f)

NON NULL AFTER:

![7](https://github.com/vidhyasrikachapalayam/Ex-01-Data-Cleaning/assets/119477817/26b2deee-916e-4285-a93b-5993073dc18b)

RESULT

Thus, the given data is read, cleansed and the cleansed data is saved into the file.


