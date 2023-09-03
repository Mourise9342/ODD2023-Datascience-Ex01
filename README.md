# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE 
```
##LOAN_DATA.CSV
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
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

##DATA_SET.CSV
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
```
OUTPUT

FOR LOAN_DATA:
DATA
```
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
```
![261767057-e56346b9-5358-4755-9fa9-0731384d7875](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/9a0ade78-9928-4a82-9872-03e7c67148bf)

NON NULL BEFORE
```
df.info()
```
![261767356-bcdd59da-892b-4b61-aea5-90c31b7fdff5](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/c089dba5-df60-4aef-b11a-645394e0aaa6)

MODE
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
```
![261767382-219a6d74-2cf9-4385-9a10-e2612b3bc28f](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/11961083-68cc-46a1-9a38-8724ae6a2fa4)
MEAN
```
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```

![261767399-326bd78c-ea1c-4502-a090-0c858b90392c](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/37208d7e-35d1-4c5c-9a1e-ab68c044f06e)
MEDIAN
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
![261767415-ff17ebcb-2b94-4fc1-a3cd-e6de2825a5e4](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/f69c55e6-2a4b-4946-809d-d9a809d769bf)
```

NON NULL AFTER
```
df.info()
```
![261767520-8b3d8ad9-670e-4765-b931-fd8f17896b07](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/4cd0d75d-5f42-4f95-83b3-6615b3bfed4b)
```
df.isnull().sum()
```
![261767531-bd92664f-5dda-4fb8-a785-24bfe8f23830](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/ae44d0fb-ab31-444c-8427-c9c1617bf0ea)

FOR DATA_SET:
DATA
```
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
```
![261767548-f088086c-bab3-4a3b-a14a-407209394c15](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/5bc617da-7b9f-4775-89e8-131cbfca8756)

NON NULL BEFORE
```
df.info()
```
![261767667-19b2df64-70aa-4b25-a0c4-e01864623991](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/9db8f17a-a991-429a-8584-f7cc911308da)
```
df.isnull()
```
![261767769-0ce02807-0898-4881-96e9-c0a05b4c3275](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/6833fe17-8a23-444b-9530-135cdd82ccda)
```
df.isnull().sum()
```
![261767803-f82ae558-0de5-4473-9f26-f57036bef55c](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/fffb901b-fd2d-4abf-bf4e-e9f479652458)

MODE
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![261767891-6a6b6c93-f4a9-4839-89a2-8c4e04f03772](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/a450d213-5aa7-4e8c-8faa-3395dbf1c6a5)

MEAN
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![261776919-d45490eb-f685-4b1d-8fbc-f2d9d32188ae](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/cd51173e-95ed-42c2-b349-df64acb92597)

MEDIAN
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![261776992-ec53fe34-539b-4abf-8a49-3a0770f1b8b6](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/a47b8cd1-be40-4579-80c0-8670e2533a88)

NON NULL AFTER
```
df.info()
```
![261777008-f38ef5d5-af1b-4c19-bd5d-14ee0427ac08](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/249d7766-0bf2-4b2a-8de2-bb7466f233d7)
```
df.isnull()
```
![261777013-4634d6c5-51ab-4972-a742-4b158c40d670](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/57152507-76ef-4605-a6f3-89f466c6d6fa)
```
df.isnull().sum()
```
![261777076-4611191e-159e-4a17-9170-8bdc523d8c93](https://github.com/Mourise9342/ODD2023-Datascience-Ex01/assets/120081893/d3b69cb4-a796-407e-a9fb-dcdd7ad3ade9)

RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.
 




