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

df=sns.load_dataset("tips")

import seaborn as sns

import matplotlib.pyplot as plt
sns.violinplot(x="day", y="total_bill", hue="smoker", data=df, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")

import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)

import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])

sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)

sns.kdeplot(data=tips, x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set2', alpha=0.8)

import numpy as np
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(data)

hms=sns.heatmap(data=data)

hms=sns.heatmap(data=data,annot=True)

import numpy as np
df=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(df)

hms=sns.heatmap(data=df)

hms=sns.heatmap(data=df,annot=True)

import seaborn as sns
import numpy as np
import matplotlib.pyplot as plt

tips=sns.load_dataset("tips")
numeric_cols=tips.select_dtypes(include=np.number).columns
corr=tips[numeric_cols].corr()

sns.heatmap(corr,annot=True,cmap="plasma",linewidths=0.5)

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

![381002060-e23ed86f-231f-4104-bab8-7c557458c683](https://github.com/user-attachments/assets/b4fc7803-fcc6-4705-b800-e79842894116)

![381002259-796aa75b-37be-4c60-aeb3-fd6ecd428e00](https://github.com/user-attachments/assets/8282a5a0-662f-4a52-a8de-e6499235277f)

![381002618-47d3db29-9ff5-4463-8d45-c8e6e45cad05](https://github.com/user-attachments/assets/8097e3a6-6b9a-4c79-93c6-951564b5a883)

![381002713-d50a0a85-01bd-4a82-81a0-56954c874cbc](https://github.com/user-attachments/assets/943864b6-a506-445f-b1f1-de9d93e6807b)

![381002871-c38e2fea-5675-4f38-ac34-b32e907e3747](https://github.com/user-attachments/assets/aa199d10-1626-45ca-a7c5-d109d0729811)

![381003007-da7b3f5a-d890-4894-b89a-eccf63b4ff58](https://github.com/user-attachments/assets/7b62c05f-b0b9-4c15-b11f-73a6ba6b97e7)

![381003143-61a01f5b-09b2-4450-937f-2a4574615e74](https://github.com/user-attachments/assets/b1cc0337-c1cd-418c-852c-421edd9d7862)

![381003332-34229625-f2e8-49a7-8e55-064ac614ba4a](https://github.com/user-attachments/assets/ee71cdc3-1bf9-4498-8760-90e4260867ae)

![381003493-aa02fd09-1647-42e7-82d5-6d15939cf3ad](https://github.com/user-attachments/assets/893ab75e-81bc-48ab-ac5e-8693f07bd925)


![381003754-9a23501d-d3d5-4b10-8be2-3d8d43cb8a54](https://github.com/user-attachments/assets/e18a992c-1c4a-466b-8976-85eda6baec73)

![381003853-6f8bc912-868f-4a8b-bc88-069d8e1bd284](https://github.com/user-attachments/assets/ff2d7170-c763-485b-b83c-577052cbe065)

![381004157-de213782-303a-4f3b-a0a1-070507eb9f73](https://github.com/user-attachments/assets/11992c24-b41b-4d24-84be-5b63cc948fd7)


# Result:
 Thus, all the data visualization techniques of Seaborn has been implemented.
