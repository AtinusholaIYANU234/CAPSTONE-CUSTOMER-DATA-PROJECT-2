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
![IMG_20241105_220119_429](https://github.com/user-attachments/assets/9feceac5-8774-416f-9b69-a89bb21d3986)

![IMG_20241105_220213_233](https://github.com/user-attachments/assets/cd78c1fb-a8c0-44a1-922a-687c7ff745b5)

![IMG_20241105_220256_839](https://github.com/user-attachments/assets/84c8d224-c746-4d85-90cb-03bfa837644e)

![Uploading IMG_20241105_221545_847.jpg…]()
![IMG_20241105_221638_187](https://github.com/user-attachments/assets/cbf72ed6-016a-46bd-9381-bede8b154494)

![IMG_20241105_221815_017](https://github.com/user-attachments/assets/b9988dbc-aee4-436a-ae44-cb9ffb2f56c5)

![IMG_20241105_221923_487](https://github.com/user-attachments/assets/9b394ac2-cd0e-4018-847f-268265c8c002)
![IMG_20241105_222257_128](https://github.com/user-attachments/assets/850d7c81-822f-4a36-b07b-4b5e3102b30e)

![IMG_20241105_222333_468](https://github.com/user-attachments/assets/96d9c905-8a04-45c7-a0b7-4e99ed32ea12)
![IMG_20241105_222402_790](https://github.com/user-attachments/assets/35e8c902-af8c-4202-a62e-4fb5a3edc370)

![IMG_20241105_222445_504](https://github.com/user-attachments/assets/665ca675-17fb-4cc3-9f8c-13bd6b33b96b)
![IMG_20241105_221815_017](https://github.com/user-attachments/assets/ac67966b-bf53-4ab7-bbd2-cd097b04adcd)


