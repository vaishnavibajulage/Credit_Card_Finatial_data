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

- Step 8 : Visual filters (Slicers) were added for weekly Date fields named "weekly_start_Date".
- Step 9 : one treeMap were added to the canvas Based on Gender,one representing Female & other representing Male
![WhatsApp Image 2024-05-10 at 01 57 35](https://github.com/vaishnavibajulage/Credit_Card_Finatial_data/assets/83158414/1b0ea45e-30f7-4e93-a2e8-07dc7e6f8880)

           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
- Step 10 : In the report view, under the insert tab, One text boxe added to the canvas, in that  CREDIT  CARD  CUSTOMER REPORT  was mentioned .
 
- Step 11 : Calculated column was created in which, customers were grouped into various age groups.

for creating new column following DAX expression was written;
       
Age Group =  SWITCH(TRUE(),
'cc_bb customer'[Customer_Age]<30,"20,30",
'cc_bb customer'[Customer_Age]>=30 && 'cc_bb customer'[Customer_Age]<40,"30-40",
'cc_bb customer'[Customer_Age]>=40 && 'cc_bb customer'[Customer_Age]<50,"40-50",
'cc_bb customer'[Customer_Age]>=50 && 'cc_bb customer'[Customer_Age]<60,"50-60",
'cc_bb customer'[Customer_Age]>=60,"60+",
"unknnown"
)   

![WhatsApp Image 2024-05-10 at 09 34 49](https://github.com/FusionIIIT/Fusion/assets/83158414/b1686346-e606-41d1-b8be-724a1e7103ef)


        
- Step 15 : New measure was created to find total income.

Following DAX expression was written for the same,
        
incomeGroup = SWITCH(TRUE(),
'cc_bb customer'[Income]<35000,"Low",
'cc_bb customer'[Income]>=35000&& 'cc_bb customer'[Income]<70000,"med",
'cc_bb customer'[Income]>=70000 ,"High"
) 
        


![snapshort](https://github.com/FusionIIIT/Fusion/assets/83158414/7998bad7-97b9-431f-a2af-ccc3dc362ab6)

Step 11 : Calculated column was created in which, that is week2

for creating new column following DAX expression was written;
![Snapshort](https://github.com/FusionIIIT/Fusion/assets/83158414/6961a9d5-3c28-463e-84de-864697a0c9df)

# Snapshot of Dashboard (Power BI Service)
![Dashboard](https://github.com/FusionIIIT/Fusion/assets/83158414/77524d69-d729-4d12-bc2c-e802c2ec724e)


A card visual was used to represent Total Revenue,Total Intrest,Income,css.

![WhatsApp Image 2024-05-10 at 10 14 14](https://github.com/FusionIIIT/Fusion/assets/83158414/06213ff7-13a1-4fb0-a1db-81967df026b0)


 
 # Report Snapshot (Power BI DESKTOP)

 
![Dashboard_upload](https://github.com/FusionIIIT/Fusion/assets/83158414/ec3b7d3f-91e2-48ae-8cc6-13b9030e0f74)


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

          

    
 
  
  
  

 
