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
"""EX NO6: Data visualization Using Seaborn"""

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

# Datas
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]

# Create line plot using seaborn
sns.lineplot(x=x, y=y, marker='o')
plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.title("Line Plot Using Seaborn")
plt.show()

# Multiple line plots
x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]

# implement line plot and include all the necessary parameters
plt.figure(figsize=(8,5))

sns.lineplot(x=x, y=y1, marker='o', label='y1')
sns.lineplot(x=x, y=y2, marker='s', label='y2')
sns.lineplot(x=x, y=y3, marker='^', label='y3')

plt.xlabel("X Values")
plt.ylabel("Y Values")
plt.title("Multiple Line Plot Using Seaborn")
plt.legend()
plt.grid(True)
plt.show()

"""Bar Plot - Seaborn"""

tips = sns.load_dataset('tips')

# Implement Bar plot with hue parameter
plt.figure(figsize=(8,5))
sns.barplot(x='day', y='total_bill', hue='sex', data=tips)

# Set labels and title
plt.xlabel("Day")
plt.ylabel("Total Bill")
plt.title("Bar Plot with Hue Parameter")
plt.show()

# Include titanic dataset
tit = pd.read_csv("titanic_dataset.csv")
tit

plt.figure(figsize=(8,5))

# Implement barplot using seaborn and set x='Embarked',y='Fare',
# data=tit, palette='rainbow' and set graph title
# as "Fare of Passenger by Embarked Town"

sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')

plt.title("Fare of Passenger by Embarked Town")
plt.show()

plt.figure(figsize=(8,5))

# Implement barplot using seaborn and set
# x='Embarked',y='Fare',data=tit,
# palette='rainbow',hue='Pclass'
# and set graph title as
# "Fare of Passenger by Embarked Town, Divided by Class"

sns.barplot(x='Embarked', y='Fare', data=tit,
            palette='rainbow', hue='Pclass')

plt.title("Fare of Passenger by Embarked Town, Divided by Class")
plt.show()

# using tips dataset implement Scatter plot of total bill vs tip amount
plt.figure(figsize=(8,5))

sns.scatterplot(x='total_bill', y='tip', data=tips,
                hue='sex', style='time', s=100)

# Set labels and title
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
plt.show()

"""VIOLIN PLOT"""

# implement violinplot by comparing any two values from titanic data set
plt.figure(figsize=(8,5))

sns.violinplot(x='Pclass', y='Age', data=tit, palette='Set2')

plt.title("Violin Plot of Age by Passenger Class")
plt.show()

"""HISTOGRAM"""

import seaborn as sns
import numpy as np
import pandas as pd

np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)

# Generating dataset of random numbers
np.random.seed(1)
num_var = np.random.randn(1000)
num_var = pd.Series(num_var, name="Numerical Variable")
num_var

# IMPLEMENT HISTOGRAM
plt.figure(figsize=(8,5))

sns.histplot(num_var, bins=30, kde=True)

plt.title("Histogram of Numerical Variable")
plt.xlabel("Values")
plt.ylabel("Frequency")
plt.show()

# IMPLEMENT histplot in seaborn and set parameters
# data=df,x=Pclass,hue=Survived,kde=True

plt.figure(figsize=(8,5))

sns.histplot(data=tit, x='Pclass', hue='Survived', kde=True)

plt.title("Histogram of Passenger Class with Survival")
plt.show()
```
<img width="659" height="782" alt="image" src="https://github.com/user-attachments/assets/6fbf70fb-3909-431b-bc0d-853cd97e2870" />
<img width="636" height="795" alt="image" src="https://github.com/user-attachments/assets/f2c8c8b5-3272-4df3-a42e-de794dfc1f91" />

<img width="648" height="803" alt="image" src="https://github.com/user-attachments/assets/69c903f2-b643-4a61-b0b4-51d41027e588" />
<img width="638" height="798" alt="image" src="https://github.com/user-attachments/assets/8b42a0bf-664f-489b-89ac-14f8f1b75a31" />
<img width="600" height="399" alt="image" src="https://github.com/user-attachments/assets/a749d61f-88cf-4579-8f70-c8f3784f25d2" />





# Result:
 Include your result here
