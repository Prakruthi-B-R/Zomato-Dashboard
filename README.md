# Zomato-Dashboard
Dashboard Link : https://app.powerbi.com/reportEmbed?reportId=b8fb4860-3ffd-4b0e-a876-6b48b70b8440&autoAuth=true&ctid=7b887c76-d8d8-4448-9bf5-a51820345eb4
Problem Statement
Design and implement a dynamic Power BI dashboard for Zomato, focusing on customer segmentation, food sales analysis, restaurant ratings, and city-wise trends. The dashboard should enable detailed exploration of customer preferences, popular cuisines, and geographic variations to drive targeted marketing strategies, optimize menu offerings, and enhance overall customer satisfaction.

Steps followed
Step 1 : Load data into Power BI Desktop, dataset is a csv file.
Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
Step 4 : Next checked for the error values and null values and replaced the null values with "Other".
Step 5 : Then used unpivot to unpivot the columns value and quantity so it can be used as a slicer for the sales analysis between the amount of sales and quantity of sales.
Step 6 : Cleaned the data set as per the requirement changing the rows as header, deleting the dupicates, changing the column name, conditional column, creating the new column where ever necessary.
