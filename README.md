# For Dashboard switch to Master Branch

<br>
<br>
<br>
<br>
<br>
<br>
<br>

# <center>Credit Card Operations Dashboard</center>

## Project Overview

This project involves the development of an interactive Power BI dashboard using transaction and customer data sourced from a SQL database. The dashboard provides real-time insights into key performance metrics and trends, enabling stakeholders to monitor and analyze credit card operations effectively.

## Project Objective

The primary objective of this project is to develop a comprehensive credit card weekly dashboard that delivers actionable insights to stakeholders. The dashboard helps in monitoring and analyzing the operations of credit cards, thereby supporting data-driven decision-making processes.

## Key Features

- **Real-Time Insights**: The dashboard is designed to provide real-time data visualization, allowing stakeholders to track the latest trends and metrics related to credit card operations.
  
- **Interactive Visualization**: Users can interact with the dashboard to explore various aspects of the data, filter results, and drill down into specific metrics.

- **Actionable Insights**: The dashboard highlights critical metrics and trends, offering actionable insights that aid in informed decision-making.

- **Streamlined Data Processing**: The data processing pipeline is optimized to ensure efficient loading and transformation of large datasets, facilitating smooth performance of the dashboard.

## DAX Functions Used

Some key DAX (Data Analysis Expressions) functions used in this project include:


  ```dax
  AgeGroup = SWITCH(
 TRUE(),
 'public cust_detail'[customer_age] < 30, "20-30",
 'public cust_detail'[customer_age] >= 30 && 'public cust_detail'[customer_age] < 40, "30-40",
 'public cust_detail'[customer_age] >= 40 && 'public cust_detail'[customer_age] < 50, "40-50",
 'public cust_detail'[customer_age] >= 50 && 'public cust_detail'[customer_age] < 60, "50-60",
 'public cust_detail'[customer_age] >= 60, "60+",
 "unknown"
 )
  ```

  ```dax
  IncomeGroup = SWITCH(
 TRUE(),
 'public cust_detail'[income] < 35000, "Low",
 'public cust_detail'[income] >= 35000 && 'public cust_detail'[income] <70000, "Med",
 'public cust_detail'[income] >= 70000, "High",
 "unknown"
)
  ```

  ```dax
  week_num2 = WEEKNUM('public cc_detail'[week_start_date])


  Revenue = 'public cc_detail'[annual_fees] + 'public cc_detail'[total_trans_amt] + 'public cc_detail'[interest_earned]
  ```

  ```dax
  Current_week_Reveneue = CALCULATE(
 SUM('public cc_detail'[Revenue]),
 FILTER(
 ALL('public cc_detail'),
 'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2]))) 

  ```

 ```dax
 Previous_week_Reveneue = CALCULATE(
 SUM('public cc_detail'[Revenue]),
 FILTER(
 ALL('public cc_detail'),
 'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2])-1))
 
  ```
- Additional DAX functions for aggregations, filtering, and time intelligence might be used, depending on the specific requirements of the dashboard.

## Dashboard Sections

The dashboard is divided into the following sections:

1. **Overview**: A high-level summary of key performance indicators (KPIs) related to credit card usage, including metrics such as transaction volumes, customer counts, and average transaction values.

2. **Trends Analysis**: Visualization of trends over time, helping stakeholders identify patterns and anomalies in credit card usage.

3. **Customer Segmentation**: Insights into customer demographics and behavior, providing a deeper understanding of customer segments.

4. **Transaction Analysis**: Detailed breakdown of transaction types, amounts, and frequencies.

## How to Use

1. **Load Data**: Ensure that the SQL database connection is active, and data is loaded into Power BI.

2. **Interact with Dashboard**: Use the filters and interactive elements to explore different metrics and visualize the data as needed.

3. **Share Insights**: Export the visualizations or share the dashboard link with stakeholders for collaborative analysis.

## Getting Started

To get started with the dashboard:

1. Open the `.pbix` file in Power BI Desktop.
2. Ensure that your data sources are correctly linked to the SQL database.
3. Refresh the data to update the dashboard with the latest information.
4. Customize the visuals and DAX formulas as needed to suit your specific business requirements.

## Conclusion

This dashboard project demonstrates the effective use of Power BI to provide real-time insights into credit card operations. The use of DAX functions enhances the interactivity and functionality of the dashboard, making it a valuable tool for decision-makers.



</br>
</br>


# Hi, I'm Supriyam Mishra! 👋





## 🚀 About Me
I'm a Data Analyst Enthusiast, have honed my skills in data analysis, visualization,
and machine learning. With hands-on experience in Python, SQL, Excel, and PowerBI, 
I am proficient in extracting insights and delivering data-driven solutions. My 
passion for data-driven decision making and problem-solving is evident in my work. 





## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/supriyam-mishra/)





## 🛠 Skills
Excel (Knowledge of Lookups, Pivot Tables, Pivot
charts and Dashboard),
Python (Knowledge of EDA and libraries like Pandas,
Numpy, Matplotlib),
SQL (Knowledge of Database principles, Joins, Subqueries, Aggregate functions, Unions),
PowerBI (Analytical & Visualization Skills, Designing
interactive charts, graphs, plots and dashboards),
Machine Learning (Basics of Machine Learning, EDA,
Data wrangling, Model training, Regression,
Classification)
