# FIFA2021
In this project, we work with a dataset from FIFA 2021 players.
Here’s a draft README file based on the details you provided:

---

# Project 1: Data Cleaning & Transformation

## Overview

The dataset is messy and requires cleaning and transformation to make it readable and useful. 

## Instructions

1. **Convert Height and Weight Columns:**
   - Convert the height and weight columns to numerical forms.

2. **Remove Unnecessary Newline Characters:**
   - Remove the newline characters from all columns that contain them.

3. **Analyze Player Tenure:**
   - Based on the 'Joined' column, check which players have played at a club for over 10 years.

4. **Convert String Columns to Numbers:**
   - 'Value', 'Wage', and 'Release Clause' columns are in string format. Convert them to numeric values. For example, "M" in the value column stands for Million, so multiply the row values by 1,000,000.

5. **Remove Star Characters:**
   - Some columns have 'star' characters. Strip these columns of these stars and make the columns numerical.

6. **Identify Underpaid Precious Players:**
   - Determine which players are valuable but still underpaid by creating a scatter plot between wage and value.

7. **Check Data Types:**
   - Verify if the height and weight columns have the appropriate data types.

8. **Separate Joined Column:**
   - Split the 'Joined' column into separate year, month, and day columns.

9. **Clean Integer Value Columns:**
   - Clean and transform integer values, wage, and release clause columns.

10. **Remove Newline Characters from Hits Column:**
    - Remove the newline characters from the Hits column.

11. **Separate Team Contract Column:**
    - Consider whether to separate the Team Contract column into separate team and contract columns.

## Recommended Tools

- **Python** or **Excel**

### Excel Instructions

1. **Convert Height and Weight:**
   - We have converted the Height and Weight columns to numbers.

2. **Remove Newline Characters:**
   - Select all cells with values (Ctrl+A). Open the "Find and Replace" dialog (Ctrl+H). In the "Find what" field, type `Ctrl+J` (newline character). Leave the "Replace with" field empty and click "Replace All."

3. **Calculate Tenure:**
   - Added a new column "Years at the Club" with the formula: `=DATEDIF(R2, DATE(2021,1,1),"Y")`. Set the format to 'Number'. Highlight cells with players who have been at a club for over 10 years using Conditional Formatting.

4. **Convert Wage and Release Clause:**
   - Changed wage and release clause columns by replacing the Euro Sign and using the formula: `=TEXT(VALUE(SUBSTITUTE(SUBSTITUTE(Z2, "K", ""), "€", "")) * 1000, "0") & "€"`. Adjusted for "M" in a similar way.

5. **Check Data Types:**
   - Verified that Height and Weight columns are in the correct 'Number' format.

6. **Separate Joined Column:**
   - Split the "Joined" column into separate Month, Day, and Year columns using appropriate formulas. Formatted each column to 'Number'.

7. **Clean Hits Column:**
   - Used `=TRIM(SUBSTITUTE(CG, CHAR(10), ""))` to remove newline characters. Created a cleaned column without the "K" sign using the formula: `=IF(RIGHT(CF2,1)="K", LEFT(CF2, LEN(CF2)-1) * 1000, CF2)`.

### Final Checks

1. **Check for Consistency and Accuracy:**
   - Verify data types: Dates should be in date format, numbers should be numeric, and text should be in text format. Use "Text to Columns" if needed.
   - Check for errors or inconsistencies and correct them.

2. **Handle Missing or Blank Values:**
   - Identify missing data using filtering or conditional formatting. Fill or replace missing values as needed.

3. **Validate Data Ranges and Logical Checks:**
   - Ensure values fall within expected ranges. Apply logical tests to verify data validity.

4. **Remove Duplicates:**
   - Use Excel's "Remove Duplicates" feature to ensure no duplicate rows exist unless expected.

5. **Review Data Formatting:**
   - Ensure proper and consistent formatting, especially when combining multiple data sources. Remove extra spaces using the TRIM function.

---

Feel free to adjust or add any additional details as needed!
