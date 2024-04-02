# Excel Bike Sales Project

This Excel project aims to showcase certain trends that help a bike company understand their customers better which can help in increasing their sales. In this project, we look at a bike purchases dataset where we have information such as age, marital status, gender, education and more for each of the customers who made a purchase from a bike company. I started with cleaning the data, then analyzing it and creating pivot tables for different trends that can shed light on a customer's preferences and choices when it comes to buying a bike. I then used those pivot tables to create a bike sales dashboard for stakeholders.


## I. Cleaning the data:

1. Removed duplicates by selecting the entire dataset and using the 'Remove Duplicates' built-in function in Excel. 
2. Replaced the strings 'S' and 'M' in the Marital Status column with the strings 'Single' and 'Married' respectively.
3. Replaced the strings 'M' and 'F' in the Gender column with the strings 'Male' and 'Female' respectively.
4. Converted the values in the Income column to currency as well as decreased the decimal places to 0 (since the income values are all round numbers anyways).
5. Replaced the string 'Bachelors' with the string "Bachelor's".
6. Added a new column for Age Brackets since the data contains customers ranging from 25-89 years old, which can make it difficult to visualize. Creating age groups will help in creating a cleaner visualization. To create the age brackets I used the following formula:

**=IF(L2>=65, "Elderly 65+",IF(L2>=40, "Middle Age 40-64", IF(L2<40, "Adolescent 0-39", "Invalid")))**

The above formula is a nested IF statement that uses conditions that will return a certain result if true. For example, for **IF(L2<40, "Adolescent 0-39", "Invalid")**, if the age in the cell is less than 40 then replace the cell with the string "Adolescent 0-39". If the conditional statement is false (e.g. the age is NOT below 40) then the cell will be replaced with the string 'Invalid'.

Age brackets:
A. Adolescent - for people who are 39 y.o or below.
B. Middle Age - for people who are 40-64 y.o.
C. Elderly - for people who are 65 and above.


## II. Analyzing the data and creating a bike sales dashboard:

### Vizualization #1: Bike Purchase Comparison per Gender & Avg. Income

This bar chart explores how does income/gender affect a customer's choice to buy/not to buy a bike. It compares men VS. female customers with different incomes, and reveals the following results:

1. People with a higher average income are more likely to purchase a bike, while people with lower average income are less likely to purchase a bike. 
2. The average income of men is higher than the average income of women.

### Visualization #2: Bike Purchase Comparison by Age Group

This line chart shows how age affects a customer's choice to buy/not to buy a bike by comparing 3 different age groups and the amount of bikes purchased for each age group. The graph reveals that the people who buy the most bikes are between 40 and 64 years old, and the people who buy the least amount of bikes are 65+ years old. It could be assumed that elderly people commute less than people from younger age groups, but this is not conclusive. The adolescent group of people between 0 and 39 years old buy less bikes than the middle age group. It is possible that the people from the adolescent age group commute greater distances for which a bike wouldn't be as useful as a car, for example. 

### Visualization #3: Customer Commute

This line chart demonstrates how commute distance affects a customer's choice to buy/not to buy a bike. It compares the commute distance for people who have purchased a bike and for people who haven't purchased a bike. The graph reveals that the people who commute the shortest distances (0-1 miles) are more likely to purchase a bike. This might be the case for people whose workplace/school is close to their place of residence in which case a bike would be much cheaper than a car. Also, a bike could be more convinient in terms of parking. If we use the region filter, we could see that it's very common for people who commute short distances to own a bike in Europe. To further understand our customers across the globe, we could further analyze data about available bike parking spots and cycling roads in different countries. This will allow us to understand how convinient it is to use a bike in a given region.








