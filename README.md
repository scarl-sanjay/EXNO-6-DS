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


      import pandas as pd
      import seaborn as sns
      import matplotlib.pyplot as plt
      df=pd.read_csv("titanic_dataset.csv")
      df.head()




![328475114-79f4819c-dfc3-4906-84c0-9e03ce115c32](https://github.com/user-attachments/assets/ff246e8a-2d10-44b7-bcee-20210556cfa5)



1.Line Plot


      x=[1,2,3,4,5]
      y=[3,6,2,7,1]
      sns.lineplot(x=x,y=y)
      plt.title('Line Plot')





![328475177-68a63045-f6dc-4229-bc53-e4e4e71b14f5](https://github.com/user-attachments/assets/039930a2-701d-4eb0-88bb-d0953bfa4634)



2.Multi Line Plot



      x=[1,2,3,4,5]
      y1=[3,5,2,6,1]
      y2=[1,6,4,3,8]
      y3=[5,2,7,1,4]
      sns.lineplot(x=x,y=y1)
      sns.lineplot(x=x,y=y2)
      sns.lineplot(x=x,y=y3)
      plt.title('Multi Line Plot')





![328475234-aae1a706-a5b2-41ed-bd91-3bfde2f18fae](https://github.com/user-attachments/assets/394e0b91-1091-40ab-82d7-6712f6c0ed6b)



TO VISUALIZE RELATIONSHIPS


1.Bar Chart


      plt.figure(figsize=(8,5))
      sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
      plt.title("Fare Of Passenger By Embarked Town")


![328475304-5b1aa904-42d7-47dc-8ad2-9803d35a864f](https://github.com/user-attachments/assets/b72d36e2-754d-49f2-91ca-24c77332f24d)


2.Scatter Plot

    sns.scatterplot(x="Age", y="Fare", data=df)
    plt.title('Scatterplot of Age vs Fare')
    plt.show()
    
    
    
    
![328475366-c7ad7761-a406-4582-931f-ad1515696c58](https://github.com/user-attachments/assets/8c787ffb-5b18-4b4f-8e9d-9c222e424f69)



3.Bubble Chart


      sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
      plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
      plt.show()



![328475416-a99cc2f3-7b66-408e-89f4-948bf9b80dda](https://github.com/user-attachments/assets/e294cc77-d04b-485b-9467-028347388d5e)



TO CAPTURE DISTRIBUTIONS


1.Histogram


    sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)



![328475479-a5f69477-e68b-4892-b3cd-965610b7faef](https://github.com/user-attachments/assets/efce6920-569d-46b0-8005-9ef2d758f93c)

2.Box Plot

      sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
      plt.title("Age By Passenger Class")


![328475542-0caa044f-a411-49e8-b05e-66cf67c49383](https://github.com/user-attachments/assets/92f9db8b-ae76-447e-8bca-e0579ab4dd87)

3.Violin Plot


    sns.violinplot(x="Pclass", y="Fare", data=df)
    plt.title('Violin Plot of Fare by Passenger Class')
    plt.show()


![328475591-b725d969-8c14-4cfc-9ef8-80035a388b93](https://github.com/user-attachments/assets/5d31b843-c672-475c-b8a4-584c39fc0d6a)


4.Density Plot

      sns.kdeplot(data=df['Age'], shade=True)
      plt.title('Density Plot of Passenger Ages')
      plt.show()


![328475671-2da67e4d-d184-4c90-8859-cca668c52057](https://github.com/user-attachments/assets/365eafce-5fbc-43df-9fa7-5d9c5ff81c1b)



5.Heatmap


      numeric_df = df.select_dtypes(include=['float64', 'int64'])
      corr_matrix = numeric_df.corr()
      sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
      plt.title('Heatmap of Titanic Dataset')
      plt.show()

![328475785-5cc6be20-4ef3-4db4-86fd-5eb9f9299a0d](https://github.com/user-attachments/assets/e224bd4e-5995-410a-b85b-314caf78f141)



Result:

Thus, the Data Visualization using seaborn python library for the given data is implemented successfully




      

