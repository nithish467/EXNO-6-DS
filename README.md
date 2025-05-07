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

![328475114-79f4819c-dfc3-4906-84c0-9e03ce115c32](https://github.com/user-attachments/assets/80466d15-4efa-4fb5-bd05-3007062fc92f)


# 1.Line Plot

      x=[1,2,3,4,5]
      y=[3,6,2,7,1]
      sns.lineplot(x=x,y=y)
      plt.title('Line Plot')

![328475177-68a63045-f6dc-4229-bc53-e4e4e71b14f5](https://github.com/user-attachments/assets/9c7d6462-e5eb-4836-a4b5-7375f5f95ac8)

# 2.Multi Line Plot

      x=[1,2,3,4,5]
      y1=[3,5,2,6,1]
      y2=[1,6,4,3,8]
      y3=[5,2,7,1,4]
      sns.lineplot(x=x,y=y1)
      sns.lineplot(x=x,y=y2)
      sns.lineplot(x=x,y=y3)
      plt.title('Multi Line Plot')
![328475234-aae1a706-a5b2-41ed-bd91-3bfde2f18fae](https://github.com/user-attachments/assets/b41a74c9-7a0d-440b-936f-d5f69a92db7d)



# TO VISUALIZE RELATIONSHIPS
# 1.Bar Chart
    
    plt.figure(figsize=(8,5))
    sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
    plt.title("Fare Of Passenger By Embarked Town")

![328475304-5b1aa904-42d7-47dc-8ad2-9803d35a864f](https://github.com/user-attachments/assets/5b96c062-0d87-4e71-aa95-0ca80823f4c2)

# 2.Scatter Plot
    
    sns.scatterplot(x="Age", y="Fare", data=df)
    plt.title('Scatterplot of Age vs Fare')
    plt.show()
![328475366-c7ad7761-a406-4582-931f-ad1515696c58](https://github.com/user-attachments/assets/0d025f19-6acb-4c3e-9fe2-9a4da7c6db58)


# 3.Bubble Chart

    sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
    plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
    plt.show()
![328475416-a99cc2f3-7b66-408e-89f4-948bf9b80dda](https://github.com/user-attachments/assets/3dec9324-bd6e-4206-acac-6b32307bfbbc)


# TO CAPTURE DISTRIBUTIONS
# 1.Histogram
    
    sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

![328475479-a5f69477-e68b-4892-b3cd-965610b7faef](https://github.com/user-attachments/assets/ca693f14-585c-4725-b6de-4293c36bd8a5)

# 2.Box Plot
    
    sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
    plt.title("Age By Passenger Class")

![328475542-0caa044f-a411-49e8-b05e-66cf67c49383](https://github.com/user-attachments/assets/ac143f76-c43f-4aaa-9420-0799d976699a)

# 3.Violin Plot

    sns.violinplot(x="Pclass", y="Fare", data=df)
    plt.title('Violin Plot of Fare by Passenger Class')
    plt.show()
![328475591-b725d969-8c14-4cfc-9ef8-80035a388b93](https://github.com/user-attachments/assets/c85bdb6b-cbb1-44ac-933c-ff9a8ff04502)


# 4.Density Plot

    sns.kdeplot(data=df['Age'], shade=True)
    plt.title('Density Plot of Passenger Ages')
    plt.show()
![328475671-2da67e4d-d184-4c90-8859-cca668c52057](https://github.com/user-attachments/assets/8577a83e-8187-4696-b9af-e1866502a149)


# 5.Heatmap

    numeric_df = df.select_dtypes(include=['float64', 'int64'])
    corr_matrix = numeric_df.corr()
    sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
    plt.title('Heatmap of Titanic Dataset')
    plt.show()
![328475785-5cc6be20-4ef3-4db4-86fd-5eb9f9299a0d](https://github.com/user-attachments/assets/f6832c3d-c2b9-4f25-ba38-5764c3f215ce)


# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
