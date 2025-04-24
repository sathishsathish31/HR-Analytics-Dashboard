HR Analytics Dashboard 📊✨

Unlock the story behind employee data with Power BI!

Welcome to my HR Analytics Dashboard, built to explore and visualize employee attrition trends, department-wise stats, and workforce insights — all in one interactive Power BI file!

> “Data is the new oil. But refined data is rocket fuel.” 🚀
---

Project Overview 🧐

This dashboard helps answer critical HR questions:

Why are employees leaving?

Which departments face high attrition?

Does gender, marital status, or training influence employee retention?


With just a few clicks, you can filter and explore trends based on gender, department, job role, overtime, and more!


---

Dashboard Highlights ⭐
Here are some key metrics from the dashboard:

👥 Total Employees: 1470

📉 Attrition Rate: 16%

💵 Average Hourly Rate: $65.89

⏳ Average Tenure: 7.01 years

---

Key Visuals 🧩

Donut Charts: Attrition by Gender & Marital Status

Bar Graphs: Department vs Attrition

Line Charts: Training Time vs Working Years

Column Charts: Age vs Attrition (split by gender)

Filters/Slicers: Department, Job Role, Education, etc.


> Tip: Use the slicers on the dashboard to explore different employee groups and find patterns!




---

Tech Stack 🛠️

Power BI: For visualizing data interactively

Python (pandas): For cleaning & preparing the dataset

GitHub: For sharing and collaborating



---

Data Cleaning Process (Python) 🧼🐍

Before importing into Power BI, the raw data was cleaned using pandas:

import pandas as pd

#load the dataset
df=pd.read_csv("WA_Fn-UseC_-HR-Employee-Attrition (1).csv")
print(df)

# drop irrelevant colums
df.drop(columns=['EmployeeCount','Over18','StandardHours','EmployeeNumber'],inplace=True)

#Create some features
df['IsOverTime']=df['OverTime'].map({'Yes':1,'No':0})
df['AttritionFlag']=df['Attrition'].map({'Yes':1,'No':0})
df['YearsWithCompanyRatio']=df['YearsWithCurrManager']/df['TotalWorkingYears']

#fill any missing values
df.fillna(0,inplace=True)

#check missing values
df.isnull().sum()
df.to_csv("HR_Anlaytics.csv",index=False)
---

How to Use This Project 🚀

1. Clone this repo or download the .pbix file


2. Open it with Power BI Desktop


3. Explore the dashboard using slicers & filters


4. Discover key patterns in employee data!




---

Let's Connect! 🤝

Interested in data, dashboards, or just want to chat?

LinkedIn :[https://www.linkedin.com/in/sathees-kumar-k-23b3aa354]

Portfolio (coming soon!)



---

If you found this project helpful, give it a ⭐ and share it!
Feedback & suggestions are always welcome. Thanks for checking it out!
