## CAPSTONE CUSTOMER DATA PROJECT 2

### Project Title: Customer Segmentation for a Subscription Service
---
### Project Overview
Customer data for a subscription service includes a wealth of information about users that helps businesses understand and enhabce their service offerings. By leveraging customer data, subscription services can make informed decisions that drive growth, enhance customer satisfaction, and increase profitability.

### Data Sources
---
The primary source of data used here is microsoft excel worksheet by Mr Muhsin Hameed from the Ladies in Tech Africa in Conjunction with The Incubator Hub.

### Data Tools Used
- Microsoft Excel
 1. For Data Cleaning
 2. For Analysis
 3. For Visualization

- SQL- Structured Query Language for data query

- Power BI
 1. For Data Integration
 2. For Data Transformation
 3. For Data Visualization

GitHub for Portfolio Building

### Data Cleaning and Preparations
At the initial stage of the data cleaning and preparations, we carried out the following;
1. Data loading and Inspections
2. Handling missing variables
3. Data Cleaning and formatting

### Exploratory Data Analysis
---
Conducting Exploratory Data Analysis (EDA) for customer segmentation in a subscription service involves understanding the data itself, cleaning it, and identifying key patterns that can be used to group customers into meaningful segments. In this particular project, EDA was used to provide answers to some of the following questions;
- How to retrieve the total number of customers from each region
- Find the most popular subscription type by the number of customers
- Find customers who canceled their subsriptions within six months
- Calculate the total revenue by subscription type
- Find the total number of active and canceled subscriptions.

### Data Analysis
---
This is where i include some basic lines of queries and formulars (excel metrics) used during the analysis  

```SQL
SELECT * FROM[dbo].[CustomerDATA ProJECT 2]
```
```SQL
SELECT Region, COUNT(customerID) AS Total_Customers
FROM[dbo].[CustomerDATA ProJECT 2]
Group By Region;
```
```SQL
SELECT SubscriptionType,
COUNT(CustomerID) AS Most_Popular_Subscription_Type
FROM[dbo].[CustomerDATA ProJECT 2]
GROUP BY SubscriptionType
ORDER BY Most_Popular_Subscription_Type
DESC
```
```SQL
SELECT CustomerName,
SubscriptionStart
SubscriptionEnd
FROM[dbo].[CustomerDATA ProJECT 2]
WHERE Canceled = 'TRUE'
```
```SQL
SELECT SubscriptionType, SUM(revenue) AS Total_Revenue
FROM[dbo].[CustomerDATA ProJECT 2]
GROUP BY SubscriptionType
```
```SQL
SELECT
 SUM(CASE WHEN canceled='TRUE' THEN 1 ELSE 0 END)AS Total_Canceled,
  SUM(CASE WHEN Canceled='FALSE' THEN 1 ELSE 0 END) AS Total_Active
FROM[dbo].[CustomerDATA ProJECT 2]
```
### Data Visualization
---
![SQL Total Number of Customers from each Region](https://github.com/user-attachments/assets/185c7c08-065b-45b6-8b3d-bff03d32f733)

![SQL Customers who canceled within 6 months](https://github.com/user-attachments/assets/2740382c-aaa5-46ea-90d1-812fe8569f8b)

![Pivot Table 1](https://github.com/user-attachments/assets/c70b65a1-37a3-4970-bd98-c13c71636b3d)

![Customer Data](https://github.com/user-attachments/assets/1fbb880b-4343-4d3f-8615-3433c9a047ba)

![Dashboard](https://github.com/user-attachments/assets/e3b73512-fc77-4ae3-b4df-c3e91e17c70f)

![Pivot Table 2](https://github.com/user-attachments/assets/0951ba77-3324-4111-b82d-b07e8dc57f28)




