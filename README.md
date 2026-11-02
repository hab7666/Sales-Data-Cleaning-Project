Data Cleaning SummaryProject: Sales Dataset Cleaning

Original File: Messy_data.csv

Final File: cleaned_sales_dataset.csvOverview

The original dataset contained 185 records and 9 columns. It had several data quality issues including missing values, inconsistent text formatting, incorrect data types, outliers, duplicate records, and multiple date formats. The following steps were performed to clean the data.Cleaning Steps
Removed Extra Spaces
Leading and trailing spaces were removed from the CustomerName, City, Product, and OrderStatus columns.
Text Standardization
The City, Product, and OrderStatus columns were converted to Title Case to maintain consistency (for example: delhi → Delhi, SHIPPED → Shipped, laptop → Laptop).
Fixed Data Type Errors
Quantity column: Text values such as “three” and “2 pcs” were converted into proper numeric values.
UnitPrice column: Commas were removed (e.g., “18,500”) and invalid entries like “unknown” were handled.
CustomerAge column: Text values such as “forty” and “29 years” were converted into numeric form.

Handled Date Inconsistencies
Multiple date formats were standardized into a single datetime format. Rows with invalid dates were removed.
Treated Missing Values
CustomerName was filled with “Unknown”
City and OrderStatus were filled with the most frequent value (mode)
Quantity, UnitPrice, and CustomerAge were filled with the median value

Handled Outliers
CustomerAge was restricted to a realistic range of 10 to 100 years
Extremely high or negative values in Quantity and UnitPrice were replaced with the median

Removed Duplicate Records
Five exact duplicate rows were identified and removed from the dataset.
Created New Feature
A new column named TotalAmount was created using the formula:
TotalAmount = Quantity × UnitPrice
Result

After completing all the cleaning steps, the dataset is now consistent, free from missing values and duplicates, and ready for analysis. The final cleaned file has been saved as cleaned_sales_dataset.csv.
