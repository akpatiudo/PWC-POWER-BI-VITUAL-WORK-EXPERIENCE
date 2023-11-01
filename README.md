## PWC-POWER-BI-VITUAL-WORK-EXPERIENCE

### CUSTOMER CHURN RETENTION ANALYSIS

![image](https://github.com/akpatiudo/PWC-POWER-BI-VITUAL-WORK-EXPERIENCE/assets/118566096/5edc2522-760c-46a4-ab37-328728151b78)

### *Introduction*
Customer Churn Retention Analysis is a Power BI Virtual Case Experience Organised by FORAGE whose slogan is “Inspiring and empowering future professionals.” I completed this internship since April 5th, 2023. I have two different works on this base on two different datasets, the dashboard to my first work is on my LinkedIn. For Data Analysis Process To make sense of any available data, a set of procedures must be completed. Identifying these procedures is essential as each stage is crucial in ensuring that the data is appropriately processed in a bid to offer useful and actionable information. Here are the steps I took in this process: 

1  	Data Source
2  	Data Preparation
3  	Data Modelling
4.	Data Analysis
5.	Data Visualization
6.	Insight

### *Problem Statement:*

This task has been undertaken so as to: - Define proper KPI's
•	Create a dashboard for the retention manager reflecting the KPI's
•	Write a short email to him (the engagement partner) explaining your findings, and include suggestions as to what needs to be changed
•	Customers who left within the last month
•	Services each customer has signed up for: phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
•	Customer account information: how long as a customer, contract, payment method, paperless billing, monthly charges, total charges and number of tickets opened in the categories administrative and technical
•	Demographic info about customers – gender, age range, and if they have partners and dependents

### *Data Source*

The dataset was provided by FORAGE, it is in data file 02 Churn-Dataset.xlsx. click on it, then click on viw raw raw to access it.

### *Data Preparation*

The raw data was loaded into Power BI Desktop, data cleaning and transformation was done in Power Query saved and proceeded to data Modelling
•	ChurnDataset is give table named:
•	ChurnDatase which has 23 columns and 7043 rows of observation
•	Data Cleaning for the dataset was done in the power query editor as follows:
•	Replaced the value is SeniorCitizen N coverted No and Y converted Yes
•	In the new table, two columns were added: one additional conditional column named loyalty using M-formula below, and non-conditional column named left-with. 
loyalty = SWITCH(TRUE(),'ChurnDataset'[tenure]<=12,"< 1 year",'ChurnDataset'[tenure]<=24,"< 2 years",'ChurnDataset'[tenure]<=36,"< 3 years",'ChurnDataset'[tenure]<=48,"< 4 years", 'ChurnDataset'[tenure]<=60,"< 5 years",'ChurnDataset'[tenure]<=72,"< 6 years")
•	Removed Unnecessary columns
•	Removed Unnecessary rows
•	Each of the columns in the table were validated to have the correct data type

### *Data Modelling*

After the preliminary stages of Data Cleaning and Data Transformation, the Data was then modelled. The image below gives more insights into this. 
![Model](https://github.com/akpatiudo/PWC-POWER-BI-VITUAL-WORK-EXPERIENCE/assets/118566096/0870d9ea-f483-4907-8638-27f1df686267)

### *Data Analysis*

The modelled data was then analysed utilizing DAX functions and measures listed below:

1	Average MonthlyCharges = AVERAGE('ChurnDataset'[MonthlyCharges])
2	Average TotalCharges = AVERAGE('ChurnDataset'[TotalCharges])
3	Churn count = CALCULATE(COUNT('ChurnDataset'[Churn]), ALLSELECTED('ChurnDataset'[Churn]),'ChurnDataset'[Churn] = "Yes")
4	Churn rate % = DIVIDE(CALCULATE(COUNT('ChurnDataset'[Churn]), 'ChurnDataset'[Churn] = "yes”), COUNT('ChurnDataset'[Churn]), 0)
5	Dependent in % = DIVIDE(CALCULATE(COUNT('ChurnDataset'[Dependents]), 'ChurnDataset'[Dependents]="Yes",'ChurnDataset'[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[Dependents]),'ChurnDataset'[Churn]="Yes"), 0)
6	Device protection in % = DIVIDE(CALCULATE(COUNT('ChurnDataset'[DeviceProtection]), 'ChurnDataset'[DeviceProtection] ="Yes", ' ChurnDataset’[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[DeviceProtection]),'ChurnDataset'[Churn]="Yes"),0)
7	Online backup in % = DIVIDE(CALCULATE(COUNT('ChurnDataset'[OnlineBackup]), 'ChurnDataset'[OnlineBackup] ="Yes", ' ChurnDataset'[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[OnlineBackup]),'ChurnDataset'[Churn]="Yes"),0)
8	Online security in % =DIVIDE(CALCULATE(COUNT('ChurnDataset'[OnlineSecurity]), 'ChurnDataset'[OnlineSecurity] ="Yes", ' ChurnDataset '[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[OnlineSecurity]),'ChurnDataset'[Churn]="Yes"),0)
9	Partner in % = DIVIDE(CALCULATE(COUNT('ChurnDataset'[Partner]),'ChurnDataset'[Partner]="Yes",'ChurnDataset'[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[Partner]), 'ChurnDataset'[Churn]="Yes"), 0)
10	Phone service in % =DIVIDE(CALCULATE(COUNT('ChurnDataset'[PhoneService]), 'ChurnDataset'[PhoneService] ="Yes", ' ChurnDataset '[Churn]="Yes"),CALCULATE(COUNT('ChurnDataset'[PhoneService]),'ChurnDataset'[Churn]="Yes"),0)
11	SenioCitizen in % = DIVIDE(CALCULATE(COUNT('ChurnDataset'[SeniorCitizen]),'ChurnDataset'[SeniorCitizen]=1,'ChurnDataset'[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[SeniorCitizen]),'ChurnDataset'[Churn]="Yes"), 0)
12	Streaming Movies in % =DIVIDE(CALCULATE(COUNT('ChurnDataset'[StreamingMovies]), 'ChurnDataset'[StreamingMovies] ="Yes", ' ChurnDataset '[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[StreamingMovies]),'ChurnDataset'[Churn]="Yes"),0)
13	Streaming TV in % =DIVIDE(CALCULATE(COUNT('ChurnDataset'[StreamingTV]), 'ChurnDataset'[StreamingTV] ="Yes", ' ChurnDataset '[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[StreamingTV]),'ChurnDataset'[Churn]="Yes"),0)
14	Tech Support in % =DIVIDE(CALCULATE(COUNT('ChurnDataset'[TechSupport]), 'ChurnDataset'[TechSupport] ="Yes", ' ChurnDataset '[Churn]="Yes"), CALCULATE(COUNT('ChurnDataset'[TechSupport]),'ChurnDataset'[Churn]="Yes"),0)

### *Data Visualization* 
Data visualization for the data analysis (DAX) was done in Microsoft Power BI Desktop:
Shows visualizations from Customer Retention analysis:

### *Customer Churn*
![image](https://github.com/akpatiudo/PWC-POWER-BI-VITUAL-WORK-EXPERIENCE/assets/118566096/ec7a1961-4913-4334-9c53-f3eefc52d4b4)

### *Customer Risk*
![image](https://github.com/akpatiudo/PWC-POWER-BI-VITUAL-WORK-EXPERIENCE/assets/118566096/38870217-301b-4d29-bddb-07ce437a6ef2)

### INSIGHTS 
As shown the data Visualization, it can be inferred that:

### *Type of contract*

Month-to-month had the highest Customers at 3875, and was 163.07% higher than One year, which had the lowest Customers at 1473, followed by Two year at 1695 and One year at 1473.  Month-to-month had 42.71% Churn Rate. One year 11.27% Churn Rate. Two-year 2.83% Churn Rate. 

### *Payment Method*
Electronic check had the highest Sum of Monthly Charges at 180,345.00 and was 154.75% higher than Mailed check, which had the lowest Sum of Monthly Charges at 70,794.30.  Sum of Monthly Charges and total Churn Rate are positively correlated with each other.  Electronic check accounted for 39.54% of Sum of Monthly Charges.  

### *Years of Contract*
At 122,629.75, < 1 year had the highest Sum of Monthly Charges and was 142.67% higher than < 4 years, which had the lowest Sum of Monthly Charges at 50,534.50.    < 1 year accounted for 26.89% of Sum of Monthly Charges.  Sum of Monthly Charges and Churn Rate diverged the most when the loyalty was < 1 year, when Sum of Monthly Charges were 122,629.28 higher than Churn Rate.  

### *Customers At Risk*
1869 customers are at the risk of churn. and the churn rate is 27% and yearly charges is $16.06M charges. and Monthly Charges is $456.12K monthly charges.

### *Churn rate by internet service*
Fiber optic had the highest Churn Rate at 41.89%, followed by DSL at 18.96% and No at 7.40%.  Fiber optic had the highest Sum of Monthly Charges at 283,284.40, followed by DSL at 140,665.35 and No at 32,166.85.

### *New Tickets*
2955 tech tickets were opened and 3632 admin tickets were opened.

### *Demographics*
49.52% are female, 50.48 % are male, 25% are senior citizens, 36% have partners and 17% are dependant

### *Recommendation*
In this case, it is important to compare the churn rate of the business to its industry's average churn rate, taking into consideration if the business is new or mature. Knowing an industry's churn rate versus that of the business is the only way to understand if a churn rate is acceptable or poor. Every industry has a different business model and, therefore, will have different acceptable churn rates.

### *What Does a High Churn Rate Mean?*
A high churn rate indicates that a business is losing significant customers, certainly more than it is bringing in. This would mean that the business is doing something wrong, whether that be delivering a poor product, having poor customer service, or a host of other negative reasons that would explain why it is losing customers fast. A high churn rate would most likely mean a company is suffering significant losses. 



