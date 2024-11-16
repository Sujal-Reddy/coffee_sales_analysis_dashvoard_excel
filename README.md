coffee sales analysis dashboard using excel

Objective: create a dashboard on total sales over time, sales by country, top 5 customers
And add a timeline and slicers on roast type, size and loyalty card.
Dataset description: The dataset contains in total 3 worksheets
Orders
Customers
Products
Orders: contains
Order id, date, cust id, product id, quantity (given)
Cust name, email, country, coffee type, roast type, size, unit price, sales (not provided)
Step 1: And using lookups we get missing data or not provided data from customers and products into orders.
Step 2: =XLOOKUP(C2,customers!A1:A1001,customers!C1:C1001,,0)
        With above formula for email we get 0 on no data availability
        So we simply replace it with empty space using if like below
        =IF(XLOOKUP(C2,customers!A1:A1001,customers!C1:C1001,,0)=0,"",XLOOKUP(C2,customers!A1:A1001,customers!C1:C1001,,0))
        Similarly gather country too using xlookups
Step 3: then using index with match we perform dynamic lookup and gather values of 
        Coffee type, roast type, size and unit price  
Step 4: simple mul formula for sales i.e unit price* quantity
Step 5: create 2 col and add full names of coffee types and roast types using multiple if functions
Step 6: format date with month name instead of number as there are American and European format for date so there might be confusion.
Step 7: number formatting
        Add $ for unit price and sales, kg to size
Step 8: check for duplicates if any remove them
Step 9: convert range into table using ctrl+T 
Step 10: pivot tables and charts and also formatting them
Step 11: adding timeline and format them
Step 12: adding slicers 
Step 13: prepare a dashboard copy paste all pivot charts here. And also timeline and slicers
          Connect all slicers and timeline with all charts. 
