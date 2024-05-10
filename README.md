# Credit_Card_Finatial_data
Credit Card Transaction and Customer Dashboard using Power BI

# Credit_Card_Financial_Dashboard


### Dashboard Link :https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/blob/main/Credit%20Card%20Transaction%20Report.pbix

## Problem Statement

This dashboard helpsTo develop a comprehensive credit card weekly dashboard that 
provides real-time insights into key 
performance metrics and trends, 
enabling stakeholders to monitor 
and analyze credit card operations 
effectively.



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 10293 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Arrival Delay".
 
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 6 : Since the data contains various Quaters, thus in order to represent Quaters, a new visual was added using the treeMap  in the visualizations pane in report view. 

- Step 7 : Visual filters (Slicers) were added for weekly Date fields named "weekly_start_Date".
- Step 8 : one treeMap were added to the canvas Based on Gender,one representing Female & other representing Male
![sNAPSHORT 1](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/54f3f4ad-019d-438c-b199-f4059b278509)


           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
- Step 9 : In the report view, under the insert tab, One text boxe added to the canvas, in that  CREDIT  CARD  CUSTOMER REPORT  was mentioned .
 
- Step 10 : Calculated column was created in which, customers were grouped into various age groups.

for creating new column following DAX expression was written;
       
Age Group =  SWITCH(TRUE(),
'cc_bb customer'[Customer_Age]<30,"20,30",
'cc_bb customer'[Customer_Age]>=30 && 'cc_bb customer'[Customer_Age]<40,"30-40",
'cc_bb customer'[Customer_Age]>=40 && 'cc_bb customer'[Customer_Age]<50,"40-50",
'cc_bb customer'[Customer_Age]>=50 && 'cc_bb customer'[Customer_Age]<60,"50-60",
'cc_bb customer'[Customer_Age]>=60,"60+",
"unknnown"
)   

![SNAPSHORT 2](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/d33869a3-1a5a-4665-b050-59c6ac198e92)


        
- Step 11 : New measure was created to find total income.

Following DAX expression was written for the same,
        
incomeGroup = SWITCH(TRUE(),
'cc_bb customer'[Income]<35000,"Low",
'cc_bb customer'[Income]>=35000&& 'cc_bb customer'[Income]<70000,"med",
'cc_bb customer'[Income]>=70000 ,"High"
) 
        


![snapshort](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/28aed0b7-4022-4f86-ab52-5c5616104aba)

Step 12 : Calculated column was created , that is REVENUE

Revenue = 'cc_bb credit_card'[Activation_30_Days]+'cc_bb credit_card'[Interest_Earned]+'cc_bb credit_card'[Total_Trans_Amt]

![Snapshort](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/07b8e8da-2124-4df1-9e55-da882f50a4d9)

Step 13 : Calculated column was created , that is week2
 
 for creating new column following DAX expression was written;

 Week Num2 = WEEKNUM('cc_bb credit_card'[Week_Start_Date]) 

![Snapshort](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/7066e62f-dbb5-432f-9ac1-13964a297dfb)

# Snapshot of Dashboard (Power BI Service)
![Dashboard](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/f0a13611-d2da-4db9-a15b-5ce1de0aa3ed)




A card visual was used to represent TOTAL REVENUE,Total INTREST,INCOME,CSS.

![WhatsApp Image 2024-05-10 at 10 14 14](https://github.com/FusionIIIT/Fusion/assets/83158414/06213ff7-13a1-4fb0-a1db-81967df026b0)


 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/5f6017f2-de0e-4432-a7ee-290574dd84ac)


# Insights

A Double page report was created on Power BI Desktop 

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 10293

Renevue generate = 54M

Total intrest = 8M

Income Generates = 588M

Number of Customer satisfied =33K

Male customers are contributing more in revenue 30M, female 24M

Blue & Silver credit card are contributing to 93% of overall 
transaction

TX, NY & CA is contributing to 68%

Overall Activation rate is 57.5%

Overall Delinquent rate is 6.06%

          

    
 
  
  
  

 
