# Power BI Assignment-4
## DAX n Data Visualization

#### 1. Calculated Columns 
  *  Created a calucalted column for 'Category Type' by joining 'Category' & 'Sub-Category' field to one in the Order Details table : "Category Type = 'Order Details'[Category]&"-"&'Order Details'[Sub-Category]"
  *  Created "Revenue" calculated column in the 'Order Details' table by multiplying Amount to Quantity.
  *  Created Calcualted column to categorize sales based on "Amount" field in the 'Order Details' table as below: 
Sales Category = IF('Order Details'[Amount]<=500,"Below Average", "Above Average")

#### 2. Calculated Measures.
  * Calculate Order Count - the "DISTINCTCOUNT" measure is used to count the unique orders in 'Order Details' table as the table contain duplicated order ids. [ Order Count = DISTINCTCOUNT('Order Details'[Order ID]) ]
  * Calculate Average Profit in Delhi: Delhi Avg Profit = CALCULATE(AVERAGE('Order Details'[Profit]),'List of Orders'[City]="Delhi")
  * Calculate Year-to-Date (YTD) Sales: A date table were created beforehand to get the calculations correct using the below formula: YTD Sales = TOTALYTD([Total Sales],'Date Table'[Date])   
#### 3. Data Visualization 

