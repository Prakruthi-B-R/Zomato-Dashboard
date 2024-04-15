# Zomato-Dashboard
Dashboard Link : https://app.powerbi.com/reportEmbed?reportId=b8fb4860-3ffd-4b0e-a876-6b48b70b8440&autoAuth=true&ctid=7b887c76-d8d8-4448-9bf5-a51820345eb4

Problem Statement :
Design and implement a dynamic Power BI dashboard for Zomato, focusing on customer segmentation, food sales analysis, restaurant ratings, and city-wise trends. The dashboard should enable detailed exploration of customer preferences, popular cuisines, and geographic variations to drive targeted marketing strategies, optimize menu offerings, and enhance overall customer satisfaction.

Steps followed :

Step 1 : Load data into Power BI Desktop, dataset is a csv file.
Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
Step 4 : Next checked for the error values and null values and replaced the null values with "Other".
Step 5 : Then used unpivot to unpivot the columns value and quantity so it can be used as a slicer for the sales analysis between the amount of sales and quantity of sales.
Step 6 : Cleaned the data as per the requirement changing the rows as header, deleting the dupicates, changing the column name, conditional column, creating the new column where ever necessary.
Step 7 : Loaded back to Power BI desktop. and data modelling was performed between the different tables.
Step 8 : Used Advance Dax Functions and created cards, various visuals, and charts to analyze the key performance of the data.

Used card visuals to Represent the Total amount, Quantity, Ratings and Total Orders.
![Screenshot 2024-04-15 213043](https://github.com/Prakruthi-B-R/Zomato-Dashboard/assets/164649454/409cda7e-ffc2-4a22-af06-12a7d66573be)

Step 9 : Used Advance DAX Formulas to filter the city into TOP N Cities which makes the users to visualize the data easily.
Step 10 : Here The table was created First.
Step 11 : Later the DAX function like Rank,  was used to filter the data into top N cities and Slicer was used to choose the cities.
DAX Function: Top_N_sales = 
                            var Rankvalue = RANKX(ALL(orders[City]),[Total_sales],,DESC) 
                            var SelectedRank = SELECTEDVALUE(Ranktable[Number])
                            return
                            if(SelectedRank=0,[Total_sales],
                            if(Rankvalue<=SelectedRank,[Total_sales],Blank()))
![Screenshot 2024-04-15 213114](https://github.com/Prakruthi-B-R/Zomato-Dashboard/assets/164649454/bfd5ede1-7320-4057-a180-c9247f4c2398)

Step 12 : And also used the Various dax function to get the Dynamic title, Lost Users, Gain Users and dynamic chart title within the Dashboard.
![Screenshot 2024-04-15 213206](https://github.com/Prakruthi-B-R/Zomato-Dashboard/assets/164649454/8ac289e0-8299-411f-ac82-8a882638ba43)

Step 13 : Created Different charts that shows sales trends by year, anlayze the consumer by age, Ratings by cities and more.

![Screenshot 2024-04-15 212737](https://github.com/Prakruthi-B-R/Zomato-Dashboard/assets/164649454/2381f5b1-376b-4760-8839-5cabbd91ea79)

![Screenshot 2024-04-15 215429](https://github.com/Prakruthi-B-R/Zomato-Dashboard/assets/164649454/5a4a1343-e7f3-4f34-b513-d438566dd9ec)

![Screenshot 2024-04-15 215459](https://github.com/Prakruthi-B-R/Zomato-Dashboard/assets/164649454/41c6517e-9eba-4efb-88f8-808c6ab699e7)





 
