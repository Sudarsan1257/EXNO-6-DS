# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1279" height="333" alt="image" src="https://github.com/user-attachments/assets/d84e25ae-34fd-4e6f-b5ae-0f4294baf3a5" />

```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```
<img width="813" height="585" alt="image" src="https://github.com/user-attachments/assets/08443556-202c-4561-8236-18a8758f5aea" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
<img width="770" height="657" alt="image" src="https://github.com/user-attachments/assets/ba8a97e7-1e45-484e-9633-b6f64c871397" />

```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```
<img width="1385" height="684" alt="image" src="https://github.com/user-attachments/assets/a4811cef-6766-46e3-94f1-70b4811f5e6d" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="784" height="559" alt="image" src="https://github.com/user-attachments/assets/dec1bebf-b8e8-47de-a481-a2e4ad7f1528" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="806" height="558" alt="image" src="https://github.com/user-attachments/assets/38183108-d686-4c3c-afdd-41ef7784d6da" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="863" height="535" alt="image" src="https://github.com/user-attachments/assets/b6da461c-42af-4868-91ae-ac2305ca1494" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="1380" height="661" alt="image" src="https://github.com/user-attachments/assets/0f0ced68-f193-4847-b306-63a02720fd31" />

```
 sns.violinplot(x="Pclass", y="Fare", data=df)
 plt.title('Violin Plot of Fare by Passenger Class')
 plt.show()
```
<img width="843" height="581" alt="image" src="https://github.com/user-attachments/assets/4b01a062-e898-42ec-972a-e30013e4e60a" />

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="916" height="681" alt="image" src="https://github.com/user-attachments/assets/6e9958ea-4316-47d9-8722-0d44aabd6d9f" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="889" height="633" alt="image" src="https://github.com/user-attachments/assets/00cb3a7f-1ae8-45a4-bcaa-fddd41a98b2b" />

# Result:
Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.


