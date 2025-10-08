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
Exploratory Data Analysis:

Name:MOHAMED TAZEEM R
Reg no:25012330
import pandas as pd
df=pd.read_csv("titanic_dataset.csv")
df

<img width="1382" height="480" alt="image" src="https://github.com/user-attachments/assets/63ae73e2-80ca-4e1e-b48b-dcfaed804cdd" />

df.shape
<img width="190" height="41" alt="image" src="https://github.com/user-attachments/assets/0f3640aa-54ba-4118-9bea-bcf70a0eb7d8" />

df.set_index("PassengerId",inplace=True)
df
<img width="1262" height="539" alt="image" src="https://github.com/user-attachments/assets/2f34245e-bacf-435b-9732-619ef0a60b71" />

df.nunique()
<img width="285" height="261" alt="image" src="https://github.com/user-attachments/assets/9c173b06-30bf-4a54-af11-405bbd8da905" />

df['Sex'].value_counts()
![WhatsApp Image 2025-10-08 at 13 36 27_6b463d32](https://github.com/user-attachments/assets/83ba735c-99ad-4bfb-8ab5-28a193ade2e2)

df.Survived.unique()
![WhatsApp Image 2025-10-08 at 13 37 13_72ce0fab](https://github.com/user-attachments/assets/cc4738ad-567d-4d62-b70d-bf12bb38d941)

df.rename(columns={"sex":"Gender"}, inplace=True)
df
![WhatsApp Image 2025-10-08 at 13 37 49_a73774a8](https://github.com/user-attachments/assets/d23950d5-b245-4978-8ea3-6d680e83d522)

import seaborn as sns
sns.countplot(data=df)
![WhatsApp Image 2025-10-08 at 13 38 04_59f66108](https://github.com/user-attachments/assets/0ebb0862-af30-4d9b-ba0e-ea7e5136c3b7)

sns.countplot(x-"Survived", hue-"Gender", data-df)
![WhatsApp Image 2025-10-08 at 13 38 17_0d6314f8](https://github.com/user-attachments/assets/9c562117-98ea-4f20-91be-c1e22b2918e7)

sns.catplot(x="Survived", hue="Gender", data=df, kind="count")
![WhatsApp Image 2025-10-08 at 13 40 06_94a27f67](https://github.com/user-attachments/assets/6eb54f0f-5608-4217-93fb-331c2a5065ee)

sns.catplot(x="Survived", hue="Gender", data=df, kind="violin")
![WhatsApp Image 2025-10-08 at 13 40 24_e250b94e](https://github.com/user-attachments/assets/c4c63228-5745-4063-b021-04da1d5a8a50)

sns.boxplot(data=df)
![WhatsApp Image 2025-10-08 at 13 40 50_9f4a6312](https://github.com/user-attachments/assets/d14810f4-f9c1-4619-b42e-7a15b4a8b465)

df.boxplot(column="Survived", by="Gender")
![WhatsApp Image 2025-10-08 at 13 41 01_44d184a2](https://github.com/user-attachments/assets/ac48e56b-10f9-44c9-a109-9a4820e078f9)

sns.scatterplot (data=df)
![WhatsApp Image 2025-10-08 at 13 41 13_23ec3820](https://github.com/user-attachments/assets/4207cb1d-98c9-46f5-84ee-bbb0a6178c1d)

sns.scatterplot(x=df['Age'],y=df['Fare"])
![WhatsApp Image 2025-10-08 at 13 41 34_a4d6462c](https://github.com/user-attachments/assets/20053324-2471-493f-85b5-3fd44bb219ba)

sns.jointplot(x='Age', y='Fare', data=df)
![WhatsApp Image 2025-10-08 at 13 41 46_4bc3974d](https://github.com/user-attachments/assets/7db8bd04-4024-4adf-bec3-bb408a215bfc)

sns.jointplot(x='Age", y='Fare', data=df, kind="kde")
![WhatsApp Image 2025-10-08 at 13 42 01_f654d9f4](https://github.com/user-attachments/assets/e43c68e0-2fed-448b-a04a-6c211c7e9c0c)

sns.jointplot(x='Age',y='Fare', data=df,kind="hist")
![WhatsApp Image 2025-10-08 at 13 42 20_d18f481a](https://github.com/user-attachments/assets/69c42d7c-1d47-4a41-a3a9-3c2da6daa7cf)

sns.pairplot(data=df)
![WhatsApp Image 2025-10-08 at 13 42 36_120f8637](https://github.com/user-attachments/assets/f7221828-7138-4446-af5d-ef1d576129d8)

corr1=df.select_dtypes(include=['number']).corr()
sns.heatmap(corr1, annot=True)
![WhatsApp Image 2025-10-08 at 13 43 09_8b55f5d5](https://github.com/user-attachments/assets/d414c0a9-5414-4450-9083-c489755496ff)

sns.catplot(x='Gender',colour='Survived',data=df,kind='count',color='green')
![WhatsApp Image 2025-10-08 at 13 43 20_cdec3489](https://github.com/user-attachments/assets/0264ff1c-24a5-427a-a2ab-eb8a47b68c20)


# RESULT

All conditions are executed successfully
