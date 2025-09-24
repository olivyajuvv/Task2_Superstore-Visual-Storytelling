SUPERSTORE - VISUAL STORYTELLING (POWER BI)

Dataset  
Original dataset: Superstore Sales Data (sample dataset often used for Power BI / Tableau projects).  

Issues Found / Notes
- Dates may have inconsistent formats  
- Some null values in Sales, Profit, or Category columns  
- Column names not always uniform (spaces, uppercase letters)  

Cleaning / Preparation Steps
1. Removed duplicate rows.  
2. Standardized text values (Category, Sub-Category, Region, State).  
3. Converted date columns to proper date format.  
4. Renamed column headers to lowercase with underscores.  
5. Created additional columns: `year`, `month`, `year_month` for time analysis.  
6. Checked for missing values in critical fields (Sales, Profit, Order Date) and handled appropriately.  

Visualizations Created 
1. KPI Cards — Total Sales, Total Profit, Profit Margin (%)  
2. Line Chart — Sales trend over months/years  
3. Clustered Bar Chart — Sales by Category, sorted highest ? lowest  
4. Filled Map — Profit by State/Region, color-coded for positive/negative performance  
5. Additional Charts — Top 10 products, seasonal sales patterns  

Key Metrics & DAX Formulas
```DAX
Total Sales = SUM('Superstore'[Sales])
Total Profit = SUM('Superstore'[Profit])
Profit Margin (%) = DIVIDE([Total Profit], [Total Sales], 0) * 100
