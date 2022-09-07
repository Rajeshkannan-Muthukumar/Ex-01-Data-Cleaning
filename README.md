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
df = pd.read_csv('Data_set.csv')
df.head(10)
df.info()
df.tail()
df.isnull().sum()
df['show_name']=df['show_name'].fillna(df['show_name'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['original_network'].mode()[0])
df.head()
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUTPUT

![1](https://user-images.githubusercontent.com/93901857/188838412-7c1a7330-564f-4146-ad7d-2374946e182f.jpg) 

![2](https://user-images.githubusercontent.com/93901857/188838435-7372325f-b10c-4c1e-9eed-cd20348c72c1.jpg)

![3](https://user-images.githubusercontent.com/93901857/188838438-b09c2922-5b1b-4fad-879b-5b5faaaa9fca.jpg)

![4](https://user-images.githubusercontent.com/93901857/188838441-95f56c97-7fe4-4147-94d5-6540e8c327d1.jpg)

![5](https://user-images.githubusercontent.com/93901857/188838443-58f80646-afac-492c-8b88-364e229d9303.jpg)

![6](https://user-images.githubusercontent.com/93901857/188838449-27d5ebb3-4b5d-4d54-a8e3-9e07b4bce570.jpg)

![7](https://user-images.githubusercontent.com/93901857/188838456-49986033-f238-4002-a3ba-8a6abeed2da2.jpg)

![8](https://user-images.githubusercontent.com/93901857/188838465-be45f0ad-9b48-4046-aa48-78c134832f3b.jpg)
