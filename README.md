Hello all, hope you're doing great regardless that very hot weather.

We shall do a small task just to practice what we have covered in the last session

We will use this data to apply the following:

1. Initial Exploration
   Load the dataset (e.g. dirty_cafe_sales.csv) into a pandas DataFrame.

Use .info(), .describe(), .head(), .isnull().sum() to get an overview of data types, missing values, and row counts.

2. Handle Missing or Placeholder Entries
   Identify columns where missing values or placeholders like "ERROR", "UNKNOWN" appear: Item, Quantity, Price Per Unit, Total Spent, Payment Method, Location, Transaction Date
   Medium
   +3
   GitHub
   +3
   Medium
   +3
   .

Replace "ERROR" and "UNKNOWN" with NaN, then decide whether to fill or drop based on context.

3. Impute Logical Relationships
   Recognize the relationship Total Spent = Quantity × Price Per Unit, and use it to fill missing values via back-calculation. Example workflows:

Price Per Unit = Total Spent / Quantity

Quantity = Total Spent / Price Per Unit or by inferring from average price per item group
Medium
.

After filling, drop any remaining rows with missing critical values if necessary.

4. Normalize Date Column
   Convert the Transaction Date column to datetime type. If entries are missing or inconsistent:

Sort by transaction date and apply forward-fill or backward-fill to impute missing dates
reddit.com
+15
Medium
+15
brettromero.com
+15
.

Ensure all dates are in a consistent format recognized by pandas.

5. Standardize Categorical Columns
   Clean up the Item, Payment Method, and Location columns:

Normalize casing (e.g. all lower‑ or upper‑case).

Strip whitespace, remove unwanted symbols.

Replace inconsistent labels with a consistent set (e.g. "card", "cash", “unknown”)
arxiv.org
+1
brettromero.com
+1
Medium
reddit.com
+1
Medium
+1
.

6. Remove Duplicates
   Use drop_duplicates() to eliminate duplicate transaction rows if they exist.

Ensure no repeated Transaction ID values.

7. Type Conversion & Validation
   Convert numeric columns (Quantity, Price Per Unit, Total Spent) to float or int after cleaning.

Check for negative or nonsensical values (e.g. quantity zero or negative price) and handle accordingly.

8. Outlier Detection (Optional)
   Plot or calculate statistical summaries to detect outliers in Quantity, Total Spent, or Price Per Unit. Decide whether to cap, drop, or investigate outliers further.

9. Feature Engineering & Derived Columns
   Optionally derive:

Revenue per Transaction (which is essentially Total Spent).

Month, Weekday, or Hour from Transaction Date.

Grouped features like avg_price_per_item, or location_category.

And of course if you have anything to add that would be great.

And we are going to submit the task on the task submission form I will share its link with you, deadline: Thursday 31/7 until 12 AM

And feel free to ask me or Eng. Abdul Majeed anything if you have any questions.
