# EX-01-Data-Cleaning-Process-using-Python
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
val=pd.read_csv("SAMPLEIDS.csv")
print(val)
val.shape
val.head(7)
val.tail()
val.info()
val.describe()
val.isnull()
val.notnull()
val.isnull().sum()
val.isnull().any()
val.dropna()
val.dropna(axis=1)
val.fillna(8)
val.fillna(method='ffill')
val.fillna(method='bfill')
val.fillna({'GENDER':'MALE','NAME':'RAJA'})
ir=pd.read_csv("iris.csv")
ir.isnull().sum()
import seaborn as sns
sns.boxplot(x='sepal_width',data=ir)
sns.boxplot(x='sepal_length',data=ir)
Q1=ir.sepal_width.quantile(0.25)
Q3=ir.sepal_width.quantile(0.75)
IQR=Q3-Q1
print(IQR)
```
# Result
<img width="333" height="37" alt="image" src="https://github.com/user-attachments/assets/c5e162f0-ada2-4e0a-adf8-32dec4159acb" />
<img width="634" height="781" alt="image" src="https://github.com/user-attachments/assets/b85f14a7-a84b-406c-a77c-1984e9085769" />
<img width="759" height="180" alt="image" src="https://github.com/user-attachments/assets/9b13d761-805f-4e3e-8e22-ab05cb75fe08" />
<img width="762" height="242" alt="image" src="https://github.com/user-attachments/assets/9425f16d-06c7-4d63-8ac7-5d7ec45c5811" />
<img width="362" height="333" alt="image" src="https://github.com/user-attachments/assets/d47a1624-61cd-4846-a619-bb9fb3c0d1ef" />
<img width="682" height="275" alt="image" src="https://github.com/user-attachments/assets/6a57d932-8780-47be-9540-237b92e0b3e6" />
<img width="638" height="677" alt="image" src="https://github.com/user-attachments/assets/99a89362-f97c-4e48-badb-fa35a3dc6cab" />
<img width="628" height="663" alt="image" src="https://github.com/user-attachments/assets/ca3041f8-2e81-48c1-97e9-68c3642a5f3e" />
<img width="330" height="534" alt="image" src="https://github.com/user-attachments/assets/c2b9d13c-8b43-469f-b2d0-2a54f4090800" />
<img width="820" height="470" alt="image" src="https://github.com/user-attachments/assets/89c2e1e0-644d-412b-94e7-40ea663a7272" />
<img width="304" height="716" alt="image" src="https://github.com/user-attachments/assets/5bc1aff5-b28f-479d-aa2c-34dc25185362" />
<img width="794" height="727" alt="image" src="https://github.com/user-attachments/assets/21e96ef9-5bd6-4942-acbe-3983b2bc4752" />
<img width="796" height="662" alt="image" src="https://github.com/user-attachments/assets/03330fce-3cc3-49e3-a5c7-31b0dd794340" />
<img width="796" height="678" alt="image" src="https://github.com/user-attachments/assets/afa07e68-0e37-46a1-913a-d250820e83eb" />
<img width="807" height="720" alt="image" src="https://github.com/user-attachments/assets/b6872775-49d5-4d4b-87b4-5b999dd92115" />
<img width="625" height="470" alt="image" src="https://github.com/user-attachments/assets/f25f2b92-1a3f-4a7f-b82a-e36fa3411257" />
<img width="649" height="519" alt="image" src="https://github.com/user-attachments/assets/8e83eef7-1059-438c-ae73-f55b65c8bf4f" />
<img width="680" height="609" alt="image" src="https://github.com/user-attachments/assets/f8b8e5b3-6432-454a-93e4-423265fd03e1" />
