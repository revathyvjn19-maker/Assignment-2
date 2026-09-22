# Assignment-2
Data Cleaning and Transformation
## Handling Missing Values
- Check for missing values in the 'Price' column. How would you handle products with missing price information?

Finding out the missing price cells by using the 
Syntax **=ISBLANK(value)**

Missing price is replaced with Median 
**=IF(ISBLANK(D2),MEDIAN(D$2:D$32),D2)**
- If there are products with missing categories, propose a strategy to impute or deal with these missing values effectively.

Missing values shows as “Unknown”
Syntax
**=IF(ISBLANK(F2), "Unknown",F2)**
	
## Correcting Inconsistent Data:
* Identify any inconsistent text formats present in the "Product Name" column.

Arranged the “Product name” column with PROPER function 
Syntax **=PROPER(B2)**
* Identify any typos present in the "Category" column.

Finding out the typo error with “F7” function 
* Use the find and replace function to standardize the text formats in the "Product Name" column and fix any typos or misspellings in the "Category" column.

Corrected the misspellings in the "Category" column with **Find and Replace** option
	
## Removing Duplicates:
* Identify any duplicate rows within the dataset based on the entirety of each row, and remove them if any.

Removed Duplicate Rows 
**Data – Remove Duplicates**
## Splitting and Merging Data:
* Split the "Product ID" column into two separate columns for " Manufacturing Date" and "Country Code". Remove unnecessary characters, if any.
Split DD-MMM-CC into Manufacturing Date and Country Code; hyphens removed from the resulting fields.
**Data – Text to Columns**
* Merge the "Brand Name" and "Product Name" columns into one column named "Product Brand".

Merged the "Brand Name" and "Product Name" columns into one column named "Product Brand" by using “ Concatenate” Function

Syntax **=CONCATENATE(C2," ",K2)**

## Number Formatting:
* Format the data type of the "Price" column to currency format. 

Currency format applied in Price column
* Format the "Manufacturing Date" column to display dates in the "DD-MM-YYYY " format. 

Product IDs contain no year, so 2026 was used as the working year for Manufacturing Date.
Syntax
**=DATE(2026,MONTH(MID(A2,4,3)&"1"),LEFT(A2,2))**
	
## Conditional Formatting:
* Apply data bar or color scales conditional formatting in the "Price" column.
**Conditional formatting – Data Bars**
* Create a custom rule for conditional formatting in the "Category" column to highlight cells where the category is "Electronics."
**Conditional Formatting -Highlight Cells Rules – Text that contains – Electronics – select the for highlight – ok**
	
