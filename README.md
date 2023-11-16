# Ex-08-Data-Visualization-
# AIM
To Perform Data Visualization on a complex dataset and save the data to a file.

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Clean the Data Set using Data Cleaning Process

## STEP 3
Apply Feature generation and selection techniques to all the features of the data set

## STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE
```
Name: PRADEEPASRI S
Reg.No: 212221220038
```
```
import pandas as pd
import seaborn as sns
from matplotlib import pyplot as plt
df=pd.read_csv("/content/Superstore - Superstore.csv (1).csv")
df.head()
df.info()
df.isnull().sum()
LINE PLOT
sns.lineplot(x="Category",y="Sales",data=df,marker='o')

sns.lineplot(x='Ship Mode', y='Category',hue="Segment",data=df)
plt.title("Multiline Plot")
plt.show()
BAR PLOT
sns.barplot(x="Category",y="Sales",data=df)

sns.barplot(x='Region', y='Sales', data=df,palette='Set1')
plt.title("Sales in different Regions")
plt.show()
SCATTER PLOT
sns.scatterplot(x='Category',y='Sub-Category',data=df)
plt.title("Scatterplot")
plt.show()

sns.scatterplot(x='Category',y='Sub-Category',hue='Segment',data=df)
plt.show()
BOX PLOT
sns.boxplot(x="Sub-Category",y="Discount",data=df)
plt.xticks(rotation=90)

sns.boxplot( x="Profit", y="Category",data=df)
POINT PLOT
sns.pointplot(x=df["Quantity"],y=df["Discount"])
VIOLIN PLOT
sns.violinplot(x="Profit",data=df)
COUNT PLOT
sns.countplot(x="Category",data=df)

sns.countplot(x="Sub-Category",data=df)
plt.xticks(rotation=90)
HISTOGRAM
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
KDE PLOT
sns.kdeplot(x="Discount", data = df,hue='Category')
Data Visualization using Matplotlib
PLOT
plt.plot(df['Region'], df['Sales'])
plt.show()
HEATMAP
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
PIE CHART
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()

df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
BAR PLOT
plt.bar(df['Category'],df.index)
plt.show()
SCATTER PLOT
plt.scatter(df["Region"],df["Profit"], c ="red")
plt.show()
BOX PLOT
plt.boxplot(x="Sales",data=df)
plt.show()
```
# OUTPUT
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/fe04168c-4c26-4d27-88dc-09755e19bf05)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/a7d565f2-a39b-451e-a4d6-1660f3e68af0)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/e2800ea2-2200-4f6d-bd98-e28ffe91c77b)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/dbaf80f7-f886-4fd6-81b9-1e37b0b2b404)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/f606d0d9-616a-488b-8c19-fbeaedbe1484)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/3cd5bfed-faf6-41eb-98d0-55dfce74dbe2)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/3d2b1588-19f8-4ddb-9552-068fbb448ebe)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/eec62dbb-5ece-4c2b-98b3-46c3cd1ed04f)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/21ec938f-7708-4423-87b6-7ffa474d6387)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/1b31c0ce-839c-43de-8ecb-b50220ea8e0a)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/6065d07c-dac5-46db-b45a-ae018d462d7b)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/0ae34f93-4c39-4d5f-adac-7e4a38d0f109)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/035d0720-6b79-442f-8e47-e82e7b0014e1)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/72f3e79a-ed8b-4812-8e7d-fe9a6efdd704)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/0ed1fbe3-9452-4ac4-afb0-af4962723cbd)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/e78e75b0-6a57-4e6e-a23d-1ce4e73b2d5b)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-08/assets/131433142/f437af3d-4316-496c-ad98-087dbc99d13d)
## RESULT
Hence, Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.








