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

# CODE and OUTPUT
import pandas as pd
df=pd.read_csv("SAMPLEIDS.csv")
df
<img width="1141" height="740" alt="image" src="https://github.com/user-attachments/assets/5e5a7e06-b11a-4460-b152-1009aadc815e" />
df.head(7)

<img width="1011" height="307" alt="image" src="https://github.com/user-attachments/assets/38f1a1c4-82c5-4de8-8650-d332448be131" />
df.tail(7)

<img width="1202" height="297" alt="image" src="https://github.com/user-attachments/assets/c28f8720-230b-4c0d-8e7b-9c72c20752d5" />
df.info()

<img width="1315" height="407" alt="image" src="https://github.com/user-attachments/assets/42dc7932-beaa-4f69-974c-6588a4f69698" />
df.describe()

<img width="1287" height="280" alt="image" src="https://github.com/user-attachments/assets/2ae881a9-51b3-477b-87ef-172013c5d009" />
df.isnull().sum()#

<img width="777" height="272" alt="image" src="https://github.com/user-attachments/assets/3c5bb19a-a1ff-462f-ba50-4e540b6a307b" />

df.isnull().any()

<img width="717" height="285" alt="image" src="https://github.com/user-attachments/assets/a955a512-ffbf-4978-920a-020f2ba1d6f7" />
df.dropna()

<img width="1427" height="477" alt="image" src="https://github.com/user-attachments/assets/8df8e08d-0e2f-474a-ad3f-f14bb96ba596" />
df.fillna(13)

<img width="1297" height="696" alt="image" src="https://github.com/user-attachments/assets/31223013-9572-4020-bafc-60f02527757e" />
df.fillna(method="ffill")

<img width="1147" height="721" alt="image" src="https://github.com/user-attachments/assets/f31619e8-72c1-41ce-9764-a1a6cc0a7813" />
df.fillna({'GENDER':'MALE','NAME':'RAKI'})

<img width="1262" height="707" alt="image" src="https://github.com/user-attachments/assets/8dd5ba33-67c8-47ac-8380-17fb55e612b1" />
import pandas as pd
df=pd.read_csv("iris.csv")
df

<img width="1347" height="572" alt="image" src="https://github.com/user-attachments/assets/4e3b4566-afa1-4889-ac37-eaad3c085f49" />
df.isnull().sum()

<img width="522" height="192" alt="image" src="https://github.com/user-attachments/assets/c6bb4c2a-b012-4cf8-bf86-dcc6e2af1d12" />
import seaborn as sns
sns.boxplot(x='sepal_width',data=df)

<img width="1157" height="596" alt="image" src="https://github.com/user-attachments/assets/a570c36b-81fb-437c-9669-08adb0388a36" />
import seaborn as sns
sns.boxplot(x='sepal_length',data=df)

<img width="1151" height="587" alt="image" src="https://github.com/user-attachments/assets/c7c45861-3856-4168-8ef6-a885de15ad73" />

import seaborn as sns
sns.boxplot(x='petal_length',data=df)

<img width="1060" height="587" alt="image" src="https://github.com/user-attachments/assets/a9c649d2-7fdc-467a-9824-fa1800bd55d7" />
import seaborn as sns
sns.boxplot(x='petal_width',data=df)

<img width="1162" height="572" alt="image" src="https://github.com/user-attachments/assets/dc0ad015-3d57-418f-8160-742926253705" />

import pandas as pd

df = pd.read_csv("iris.csv")   
Q1 = df['sepal_width'].quantile(0.25)
Q3 = df['sepal_width'].quantile(0.75)

IQR = Q3 - Q1

out = df[(df['sepal_width'] < (Q1 - 1.5*IQR)) |
         (df['sepal_width'] > (Q3 + 1.5*IQR))]# Replace with your file name
sns.boxplot(x='sepal_width',data=out)

<img width="1242" height="586" alt="image" src="https://github.com/user-attachments/assets/03a0625a-330b-4380-8ffb-b335760e09d6" />
import numpy as np 
import scipy.stats as stats 
z=np.abs(stats.zscore(df['petal_length'])) 
z

<img width="1352" height="270" alt="image" src="https://github.com/user-attachments/assets/1d16c90e-b521-4cac-b986-77997d1b850f" />
df1=df[z<3] 
df1

<img width="1122" height="457" alt="image" src="https://github.com/user-attachments/assets/3dabf43c-ad95-4a72-9eab-7b7dcae9edc4" />


##Result 
Thus the given data successfully performed data cleaning and saved the cleaned data to a file
