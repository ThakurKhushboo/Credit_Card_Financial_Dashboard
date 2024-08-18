# Credit_Card_Financial_Dashboard
Project objective : Developed a comprehensive credit card weekly dashboard that provides real-time insights into key performance metrics and trends, enabling stakeholders to monitor and analyze credit card operations effectively.

Steps to Create the Credit Card Financial Dashboard:

Imported Data to SQL Database:
Prepared CSV files for import.
Created tables in SQL to accommodate the data.
Imported CSV files into SQL, ensuring accurate data storage.
Enhanced Data Using DAX Queries:
Created meaningful data segments, such as age groups, with DAX to summarize large datasets:

AgeGroup = SWITCH(
    TRUE(),
    'public cust_detail'[customer_age] < 30, "20-30",
    'public cust_detail'[customer_age] >= 30 && 'public cust_detail'[customer_age] < 40, "30-40",
    'public cust_detail'[customer_age] >= 40 && 'public cust_detail'[customer_age] < 50, "40-50",
    'public cust_detail'[customer_age] >= 50 && 'public cust_detail'[customer_age] < 60, "50-60",
    'public cust_detail'[customer_age] >= 60, "60+",
    "unknown"
)
Applied similar logic to categorize customer income and other data points, ensuring clarity and usability across multiple scenarios.




