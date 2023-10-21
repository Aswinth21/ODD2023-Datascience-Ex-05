# Ex:05 Feature Generation
## AIM
To read the given data and perform Feature Generation process and save the data to a file.
## Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
## ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file
## PROGRAM
```
Developed by: ASWINTH T
Register Number: 212222230015
```
### For Encoding.csv file
```
import pandas as pd
df=pd.read_csv('/content/Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
### Data.csv
```
import pandas as pd
df1 = pd.read_csv("/content/data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
### BMI.csv file
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
## OUTPUT
## For encoding.csv file
### Initial data:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/e8041fd6-67db-443d-9661-6e7231ba26bc)
### Unique Value:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/c40dc0ba-bb20-4c8b-9d93-a1e863c7377c)
### Ordinal Encoder:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/9baabd2f-b224-4acf-9348-c3bcef1a057c)
### Label Encoder:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/278c45fa-b053-40f4-ace2-a51968ea19d6)
### Binary Encoder:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/baa27aa6-9aae-4bac-a0d2-46f5d73b8846)
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/50dc9fba-82d1-42f0-8152-6a44186a206b)

## For Data.csv file
### Initial data:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/5c99ad06-b628-49b7-92a8-88ca53b5fd34)
### Unique data:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/5e5fb982-3388-4540-b4a6-fe205acbb31d)
### Ordinal Encoder:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/f357bcc8-0aab-4a36-ac7f-812d455c7df8)
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/223ff160-ee55-4c41-83e0-84e0eaa30ee6)
### Label Encoder:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/070f835c-6063-43df-8e45-d2eeaf93c6b2)
### Binary Encoder:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/c116a3cd-f8f7-447f-a5d1-d4d4f9f0b728)
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/3a911d4c-886e-4801-9d4d-18e72410d25e)
## For bmi.csv file
### Initial data:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/42e72d4a-2e45-4e06-af7d-efdfb45c034b)
### Binary Encoders:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/605b85f1-09e6-48e5-b9f9-35ee74d42dbf)
### Dummies:
![image](https://github.com/Aswinth21/ODD2023-Datascience-Ex-05/assets/120236638/b036c54b-1b5e-4ccb-9c2a-eda6f194d140)
## RESULT:
The Feature Generation process was performed and saved the data to a file.# Ex:05 Feature Generation

