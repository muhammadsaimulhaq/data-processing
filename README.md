# data-processing
import pandas as pd
df=pd.read_csv("C:\\Users\\Tech Castle\\Desktop\\.vs\\Crime_Data_from_2020_to_Present.csv")
df.shape
# Data cleaning
df.info()
df.head()
df.tail()
df.isna().sum()
df.dropna()
df.dropna(inplace=True)
# Replace Empty Values
df.fillna(20)
print(df)
df.info()
df.describe()
df.iloc[3]
df['AREA'].value_counts().plot(kind="bar")
df['AREA'].value_counts().plot(kind="barh")
df['AREA'].value_counts().plot(kind="area")
df['AREA'].value_counts().plot(kind="box")
df['AREA'].value_counts().plot(kind="density")
df['AREA'].value_counts().plot(kind="pie")
df['AREA'].value_counts().plot(kind="line")
df['AREA'].value_counts().plot(kind="kde")
df.describe(include="all")
a = df['AREA']
print(a)
# Preprocessing 
df.isnull()
df.sample(3)
# Slicing in Code

df[2:3]
df[3:2:4]
df[['AREA']][1:3]
# std()-Standard Deviatoin
df['AREA'].std()
# var-Variance Calculation
df['AREA'].var
# Adding a new column in data frame 
df ['AREA']
# Remove a column
df.drop(columns=['AREA'],inplace=True)
df
# Add a row
a=pd.DataFrame({'number_courses':50,
                'Mark':'19.202',
                'time_study':'0.096'},
               index=[0])
a
df=pd.concat([a,df])
df
# Data Save
pip install openpyxl
df.to_excel("newdata.xlsx", sheet_name="newsheet")
