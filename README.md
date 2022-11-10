# Ex-07-Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
```
Name: M VIGNESH
Register.number:212220233002


import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt


df = pd.read_csv("Superstore.csv")


df.head()

df1=df.loc[:,["Ship Mode","Sales"]]

df1=df.groupby(by=["Ship Mode"]).sum()

labels=[]
for i in df1.index:
    labels.append(i)
colors = sns.color_palette('bright')
plt.pie(df1["Sales"],labels=labels,autopct = '%0.0f%%')
plt.show

df.head()

df1

df1.info()

df1=df1.groupby(by=["Category"]).sum()
labels=[]
for i in df1.index:
    plt.pie(df1["Profit"],colors = colors,labels=labels,autopct='0.0f%%')


sates=df.loc[:,["State","Sales"]]

plt.figure(figsize=(10,10))
sns.barplot(x="State",y="Sales",data=states)
plt.xticks(rotation=90)
plt.xlabel=("STATE")
plt.ylabel=("SALES")
plt.show()

sns.set_style('whitegrid')
sns.countplot(x='Segment',data= df, palette='rainbow')

sns.set_style('whitegrid')
sns.countplot(x='Category',data=df, palette='rainbow')


sns.set_style('whitegrid')
sns.countplot(x='Sub-Category',data=df, palette='rainbow')


sns.set_style('whitegrid')
sns.countplot(x='Region',data=df, palette='rainbow')


sns.set_style('whitegrid')
sns.countplot(x='Ship Mode',data=df, palette='rainbow')


category_hist = sns.FacetGrid(df, col='Ship Mode', palette='rainbow')
category_hist.map(plt.hist, 'Category')
category_hist.set_ylabels('Number')


subcategory_hist = sns.FacetGrid(df, col='Segment', height=10.5, aspect=4.6)
subcategory_hist.map(plt.hist, 'Sub-Category')
subcategory_hist.set_ylabels('Number')


grid = sns.FacetGrid(df, row='Category', col='Sub-Category', height=2.2, aspect=1.6)
grid.map(sns.barplot, 'Profit', 'Segment', alpha=.5, ci=None)
grid.add_legend()
```

# OUPUT:
![1 1](https://user-images.githubusercontent.com/53014593/200989933-49d958f6-867c-4cfc-ad7d-db87b5760437.png)
![1 2](https://user-images.githubusercontent.com/53014593/200990085-ee9aaf60-2673-4d9c-8f8a-2c19caf98220.png)
![1 3](https://user-images.githubusercontent.com/53014593/200990108-2a7cabe5-4d5d-45ba-804a-7e36aac53631.png)
![1 4](https://user-images.githubusercontent.com/53014593/200990123-9384dbb6-c13c-4f18-8b7e-c3b218180794.png)
![1 5](https://user-images.githubusercontent.com/53014593/200990132-b9bb3a40-6dfb-4954-bac7-327d110d3d91.png)
![1 6](https://user-images.githubusercontent.com/53014593/200990139-da3ba4d3-63bc-4c95-a30e-dcd476a3bb41.png)
![1 7](https://user-images.githubusercontent.com/53014593/200990143-9224780d-6a44-486a-9d63-880723da82f4.png)
![1 8](https://user-images.githubusercontent.com/53014593/200990164-d7e3324e-19a7-478d-a4e6-72d800476a9b.png)
![1 9](https://user-images.githubusercontent.com/53014593/200990172-19e71493-fb6b-40c2-8c03-251b26f9635d.png)
![1 10](https://user-images.githubusercontent.com/53014593/200990182-bb18daeb-9772-4914-b915-37740b58bafa.png)
![1 11](https://user-images.githubusercontent.com/53014593/200990253-342302c3-4c79-40aa-812f-e591295b63a8.png)
![1 12](https://user-images.githubusercontent.com/53014593/200990280-646c27ab-602a-4f03-9440-65fc01ea3a51.png)
![1 13](https://user-images.githubusercontent.com/53014593/200990308-1727f1f2-7a20-4b00-95d8-2e1b234ed06c.png)
![1 14](https://user-images.githubusercontent.com/53014593/200990345-96af72ef-3571-41cf-bfd1-505a933a13de.png)


## RESULT:
Data Visualization on a complex dataset and save the data to a file has been performed.
