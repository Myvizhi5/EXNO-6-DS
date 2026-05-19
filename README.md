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
<img width="881" height="156" alt="328475114-79f4819c-dfc3-4906-84c0-9e03ce115c32" src="https://github.com/user-attachments/assets/3469bc16-072e-4ac1-ba22-e6b76516a254" />

LINE PLOT
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="534" height="433" alt="328475177-68a63045-f6dc-4229-bc53-e4e4e71b14f5" src="https://github.com/user-attachments/assets/705d4750-0e82-4abf-aef3-64026b5a5674" />

MULTI LINE PLOT
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
<img width="534" height="433" alt="328475234-aae1a706-a5b2-41ed-bd91-3bfde2f18fae" src="https://github.com/user-attachments/assets/8d660b95-994d-48ee-860e-c14ac1668f96" />

BAR CHART

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="687" height="468" alt="328475304-5b1aa904-42d7-47dc-8ad2-9803d35a864f" src="https://github.com/user-attachments/assets/b9839f20-15fd-4d26-8deb-6c3f579b980a" />

SCATTER PLOT

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="571" height="453" alt="328475366-c7ad7761-a406-4582-931f-ad1515696c58" src="https://github.com/user-attachments/assets/2838b5fb-3510-4017-bdd6-d6a5b8db9b31" />

BUBBLE CHART
```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="571" height="453" alt="328475416-a99cc2f3-7b66-408e-89f4-948bf9b80dda" src="https://github.com/user-attachments/assets/ae6708da-b459-4306-88f3-8359c5c1a55f" />

HISTOGRAM

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="571" height="432" alt="328475479-a5f69477-e68b-4892-b3cd-965610b7faef" src="https://github.com/user-attachments/assets/88de53b4-ef06-4db4-a8f2-abce5b3b777f" />

BOX PLOT

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="563" height="453" alt="328475542-0caa044f-a411-49e8-b05e-66cf67c49383" src="https://github.com/user-attachments/assets/ce27c92d-8aa0-4cbb-8610-eebd7de0c648" />

VIOLIN PLOT

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="571" height="453" alt="328475591-b725d969-8c14-4cfc-9ef8-80035a388b93" src="https://github.com/user-attachments/assets/cad6db06-f593-48bb-b06a-bc7521115d6e" />

HEATMAP

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="597" height="503" alt="328475785-5cc6be20-4ef3-4db4-86fd-5eb9f9299a0d" src="https://github.com/user-attachments/assets/a20168ef-81fc-4e8e-8d38-76193d3cb2ed" />

DENSITY PLOT

```
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="585" height="453" alt="328475671-2da67e4d-d184-4c90-8859-cca668c52057" src="https://github.com/user-attachments/assets/9fb0bdbb-0c59-4b5b-b7e9-008bc4550ff2" />


# Result:
  Thus,to Perform Data Visualization using seaborn python library for the given datas is executed successfully.
