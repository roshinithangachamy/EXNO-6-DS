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
import seaborn as sns
import matplotlib.pyplot as plt
df=sns.load_dataset("tips")
df

sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")

avg_total_bill=df.groupby('day')['total_bill'].mean()
avg_tip=df.groupby('day')['tip'].mean()
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index, avg_total_bill, label='Total_bill')
p2=plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill ,label='Tip')
plt.xlabel('Day of the week')
plt.ylabel('Amount')
plt.title('Average Total Bill And Tip by day')
plt.legend()

avg_total_bill =df.groupby('time')['total_bill'].mean()
avg_tip= df.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2=plt.bar(avg_tip.index, avg_tip, bottom = avg_total_bill, label='Tip', width=0.4) 
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()

import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by day and gender')

import seaborn as sns
df= sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=df)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')

sns.histplot(data=df,x='day',hue='time',kde=True)

sns.boxplot(x=df['day'],y=df['total_bill'],hue=df['sex'])

sns.boxplot(x="day", y="total_bill", hue="smoker", data=df, linewidth=2, width=0.6,boxprops={'facecolor': 'pink', "edgecolor": 'red'},
          whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

```

![Screenshot 2024-10-23 113941](https://github.com/user-attachments/assets/6aa2c654-04d8-458b-bd60-26a4f9cfda64)

![Screenshot 2024-10-23 113949](https://github.com/user-attachments/assets/08e88e4e-1dc9-4509-a116-ead7df907be9)

![Screenshot 2024-10-23 114004](https://github.com/user-attachments/assets/04e280ec-a231-472c-b2e4-9b5a4efa43f8)

![Screenshot 2024-10-23 114014](https://github.com/user-attachments/assets/2ea5343b-34f2-4783-8311-1f1f184ae9f3)

![Screenshot 2024-10-23 114022](https://github.com/user-attachments/assets/966d41b6-cc9e-43d4-a291-783f45991fcd)

![Screenshot 2024-10-23 114030](https://github.com/user-attachments/assets/d30c0c7e-08ca-477c-9e16-1ae745015960)

![Screenshot 2024-10-23 114043](https://github.com/user-attachments/assets/b4af58ee-9455-4db9-83ce-1d16247e6e7f)

![Screenshot 2024-10-23 114051](https://github.com/user-attachments/assets/ee0cb3cd-e2cd-446c-8720-225fb5e238a7)

![Screenshot 2024-10-23 114101](https://github.com/user-attachments/assets/d25d6d55-7f19-492e-8d09-cadea5fcc840)


# Result:
 Thus, all the data visualization techniques of Seaborn has been implemented.
