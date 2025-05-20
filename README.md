# EXNO2DS
## Name : K MADHAVA REDDY
## rEG nO : 212223240064
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

## CODING AND OUTPUT:
### Importing required libraries:
```py
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
```
### Replacing the null values using mode/median/mean:
```py
# Check for nulls
print(df.isnull().sum())

# Replace any found nulls (none found here, but example for median replacement)
# df['column_name'] = df['column_name'].fillna(df['column_name'].median())
```
### Boxplot to analyze outliers
```py
plt.figure(figsize=(12, 6))
sns.boxplot(data=df[['area', 'bedrooms', 'bathrooms', 'stories', 'parking']])
plt.title("Boxplot for Numeric Features")
plt.show()
```
### Output:
![image](https://github.com/user-attachments/assets/0a3d6593-6aa7-438c-994a-d3131044d6e0)
### Countplot for categorical features:
```py
plt.figure(figsize=(12, 6))
sns.countplot(x='furnishingstatus', data=df)
plt.title("Count of Furnishing Status")
plt.show()
```
### Output:
![image](https://github.com/user-attachments/assets/ebc9eee8-117f-40da-96d1-19cf6f9d35c7)
###  Displot for univariate distribution:
```py
sns.displot(df['price'], kde=True, bins=30)
plt.title("Distribution of House Prices")
plt.show()
```
### Output:
![image](https://github.com/user-attachments/assets/bc84e979-a999-4994-877b-6d340f8711d0)
### Cross-tabulation analysis:
```py
cross_tab = pd.crosstab(df['furnishingstatus'], df['airconditioning'])
print(cross_tab)
```
### Output:
![image](https://github.com/user-attachments/assets/cdd29bdf-b216-4945-b4d6-0a5aee5670e8)
### Heatmap to show relationships:
```py
plt.figure(figsize=(10, 6))
sns.heatmap(df.select_dtypes(include=np.number).corr(), cmap='coolwarm', annot=True, linewidths=0.5)
plt.title('Correlation Heatmap')
plt.show()

```
### Output:
![image](https://github.com/user-attachments/assets/482f9b6c-6a15-42a1-898f-0fe768eae6c5)

# RESULT
I cleaned the dataset by checking for missing values and removing outliers using IQR. I performed visual and statistical EDA using boxplots, countplots, displot, crosstab, and heatmap to understand variable distributions and relationships.
