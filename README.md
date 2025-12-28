# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
import pandas as pd df=pd.read_csv("C:\Users\admin\Downloads\titanic_dataset.csv") df 
     <img width="1022" height="441" alt="Screenshot 2025-12-28 083836" src="https://github.com/user-attachments/assets/2ad8f3d5-ebd4-4bce-bf55-9a927fd31559" />

 df.shape
 <img width="1033" height="65" alt="Screenshot 2025-12-28 083915" src="https://github.com/user-attachments/assets/aadf7ae8-d3fe-4bce-a3da-f818514cd045" />

 df.set_index("PassengerId",inplace=True) df
<img width="1025" height="463" alt="Screenshot 2025-12-28 084016" src="https://github.com/user-attachments/assets/f8394fe1-9536-4747-bb35-97ebe4811afe" />

df.unique() 
<img width="1031" height="289" alt="Screenshot 2025-12-28 084032" src="https://github.com/user-attachments/assets/b4837f59-1483-410d-a2f1-e9064b3b4be5" />

df['Survived'].value_counts()
<img width="1031" height="114" alt="Screenshot 2025-12-28 084041" src="https://github.com/user-attachments/assets/96d8479f-5e8a-4505-bef3-2a8dfe38fab1" />

df.Pclass.unique()
<img width="1016" height="67" alt="Screenshot 2025-12-28 084055" src="https://github.com/user-attachments/assets/3c0f1f76-3b33-4ae9-af6c-22eb2cc7248c" />

df.rename(columns={"Sex":"Gender"},inplace=True) df
<img width="1024" height="450" alt="Screenshot 2025-12-28 084209" src="https://github.com/user-attachments/assets/21a72a38-50b2-4edd-ad67-8184dae2a2f8" />

import seaborn as sns sns.countplot(data=df)
<img width="1033" height="509" alt="Screenshot 2025-12-28 084226" src="https://github.com/user-attachments/assets/d66b94a3-b3f2-4436-8a90-9b23ffbe1d3c" />

sns.countplot(x="Survived",hue="Gender",data=df)
<img width="1036" height="564" alt="Screenshot 2025-12-28 084238" src="https://github.com/user-attachments/assets/043a48d7-ca1c-49b7-a0af-66e38aa0e40a" />

sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
<img width="1028" height="559" alt="Screenshot 2025-12-28 084250" src="https://github.com/user-attachments/assets/7578e32a-293f-483e-a7be-98a0c8e4009b" />

sns.boxplot(data=df)
<img width="1017" height="604" alt="Screenshot 2025-12-28 084302" src="https://github.com/user-attachments/assets/1b80c0fd-d8ae-46f0-a444-15b49281fa5e" />

df.boxplot(column="Survived",by="Gender")
<img width="1030" height="590" alt="Screenshot 2025-12-28 084314" src="https://github.com/user-attachments/assets/98094389-929d-4c86-9cc6-11606a897908" />

sns.scatterplot(data=df)
<img width="1037" height="483" alt="Screenshot 2025-12-28 084329" src="https://github.com/user-attachments/assets/d1f4e5ea-ea87-455a-9ec4-0cacf26f2f20" />

sns.scatterplot(x=df['Age'],y=df['Fare'])
<img width="1032" height="481" alt="Screenshot 2025-12-28 084347" src="https://github.com/user-attachments/assets/7c887d0d-c992-418c-b929-fa558242b5ee" />

sns.jointplot(x='Age',y='Fare',data=df,kind='kde')
<img width="1030" height="638" alt="Screenshot 2025-12-28 084406" src="https://github.com/user-attachments/assets/4d6bee28-fef5-4404-8b0f-ef792d061843" />

sns.jointplot(x='Age',y='Fare',data=df,kind='hist') 
<img width="1043" height="630" alt="Screenshot 2025-12-28 084429" src="https://github.com/user-attachments/assets/68db927a-538b-47f6-bacf-c463ba1df6ba" />

# RESULT
The EDA process has been done successfully
