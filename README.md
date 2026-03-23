## UPI-Transaction-Data-Analysis

### Dashboard Link : https://app.powerbi.com/groups/4d9b4f5a-92d0-4d8b-a7cc-360832421e66/reports/51c22b17-be25-42be-a39e-b6a5bb5e1a98/1be19f9e4659495082d0?experience=power-bi&bookmarkGuid=b2956cea62f20c56caa6

## Problem Statement

This dashboard provides a comprehensive analysis of UPI transactions by capturing key factors such as bank interactions, customer demographics, merchant details, and transaction types. It uses line charts to track trends over time and column charts to compare different segments. By analyzing patterns in payment methods and purposes, it helps identify user behavior and potential gaps in the system. This enables organizations to enhance digital payment strategies, improve efficiency, and deliver a better customer experience.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a Excel file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 4 : It was observed that i have to Add a Page & Age group column 
        - create new column Using DAX 

         Age groups = if('UPI Transaction'[CustomerAge]<=25 , "A1" , IF('UPI Transaction'[CustomerAge]<=35,"A2","A3"))


- Step 5 : Adding a four different chart to see the transaction 
        - Line Chart For Amount (Transaction by month [ Line Chart ])
        - Column Chart For Amount (Transaction by month [ Column Chart ])
        - Line Chart For Balance (Balance by month [ Line Chart ])
        - Column Chart For Balance  (Balance by month [ Column Chart ])

- Step 6 : In the report view, Added switchs between column chart & line Chart.

- Step 7 : A new visual was added using Matrix visualizations pane in report view. 
        - select amount 
        - remaining balance 
        - Transaction date 
        and use column formating .

        used - Amount ,  remaining balance , transaction date ,city & currency  using Filters .


- Step 8 :  Syncing Slicers & apply conditional formating .
         ' it has been applied for one to another page '
    

- Step 9 : Two Pages were added to see the transaction & Balance, one representing Line Chart for Transaction & Balance by month.
           Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration.
           
           Although, by default, entire have shown.

        Also used Conditional Formating for Cell Element to see the exact data in Color format.


- Step 10 : ADDING BOOKMARK for Transaction .
        ' it gives us flexiblity to swicth two different chart . '

        ' if you when we click on line chart amount bookmarks so in that case column chart should not be visible' 

        so now in that user will provide flexiblity to switch between two different charts .


- Step 11 : Created for NAVIGATOR to go to see the any visuals .
        - Line Chart Balance  
        - Column Chart Balance  
        - Line Chart Amount 
        - Column Chart Amount 
        
            

 - Step 12 : The report was then published to Power BI Service.
 
 
# Snapshot of Dashboard (Power BI Service)

    - Matrix Visual

![dashboard_snapo]
https://github.com/user-attachments/assets/6e9d85f9-2508-4fcf-807f-17fb7fc6952a 

 
 # Report Snapshot (Power BI DESKTOP)

    - Line Chart Amount Visual ( Transaction by month )
![Dashboard_upload]
https://github.com/user-attachments/assets/52fc010c-c9cf-447c-9a85-2e123c2dc0be


 # Report Snapshot (Power BI DESKTOP)
    - Column Chart Amount Visual ( Transaction by month )
![Dashboard_upload]
https://github.com/user-attachments/assets/4e9f0ff3-13d5-4189-9ef3-9041fcca1108




 # Report Snapshot (Power BI DESKTOP)
    - Line Chart Balance Visual ( Balance by month )
![Dashboard_upload]
https://github.com/user-attachments/assets/23636e71-655b-4f56-a3e6-c68e16667bd7




 # Report Snapshot (Power BI DESKTOP)
    - Column Chart Balance Visual ( Balance by month )
![Dashboard_upload]
https://github.com/user-attachments/assets/8d659425-f318-493c-9ba0-58832cfa4e1f



# Insights
A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

[1] Total Number of Transactions = 20000

Number of transactions by Male users = 10000

Number of transactions by Female users = 10000

Number of transactions via Mobile devices = 6666 (33%)

Number of transactions via other devices = 13334 (67%)

thus, majority of users prefer mobile devices for UPI transactions due to convenience.

[2] Bank-wise Transaction Analysis

a) Top Sending Bank = Axis Bank, ICICI Bank , HDFC Bank , SBI Bank 

b) Top Receiving Bank = Axis Bank, ICICI Bank , HDFC Bank , SBI Bank 

c) Least used Bank (Sender) = ICICI BANK 

d) Least used Bank (Receiver) = SBI BANK 

thus, certain banks dominate UPI transactions indicating higher user trust and volume.

“I used TOPN with COUNTROWS to identify highest transaction contributing banks and used CONCATENATEX to extract the bank name dynamically.”

[3] Payment Method Distribution

a) UPI ID Payments = 33.43 %

b) QR Code Payments = 33.16 %

c) Mobile Number Payments = 33.41 %

thus, most users prefer [UPI Payments method] for quick and convenient transactions.

[4] Transaction Type Insights

a) Peer-to-Peer (P2P) Transactions = 50 %

b) Merchant Payments (P2M) = 50 %

thus, majority transactions are [P2P/P2M], showing primary usage behavior of users.

[5] Purpose of Transactions

a) Shopping = 0.2 20%

b) Bills Payment = 0.2 20%

c) Travel = 0.2 20%

d) Food = 0.2 20%

e) Others = 0.2 20%

thus, most transactions are made for [top purpose], indicating key usage trends.

[6] Age Group Analysis

a) 18–25 (A1)= 15 %

b) 25–35 (A2)= 25 %

c) 35 to Above (A3)= 60 %


thus, maximum users belong to [A3 age group], showing active digital payment adoption.

[7] City-wise Transactions

a) Top City = 25.43%

b) Second Top City = 25.35%

c) Least Active City = 24.7%

thus, urban areas contribute the highest transaction volume.

[8] Merchant Analysis

a) Top Merchant (Zomato) Most frequent transaction category = 20.12%

thus, users frequently transact with popular merchants for daily needs.

[9] Device Usage

a) Laptop = 33.16 %

b) Mobile = 33.43 %

c) Tablet = 33.41 %

thus, majority of users prefer Mobile devices for UPI transactions.

[10] Key Observations

UPI transactions are highly concentrated among young and middle-aged users.

Mobile devices dominate transaction activity.

Certain banks and merchants drive most of the transaction volume.

Digital payments are primarily used for daily expenses and transfers.


