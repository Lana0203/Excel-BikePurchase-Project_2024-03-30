# Excel-BikePurchase-Project_2024-03-30

This Excel project aims to showcase certain trends that help a bike company understand their customers better which can help in increasing their sales. In this project, we look at a bike purchases dataset where we have information such as age, marital status, gender, education and more for each of the customers who made a purchase from a bike company. I started with cleaning the data, then analyzing it and creating pivot tables for different trends that can shed light on a customer's preferences and choices when it comes to buying a bike. I then used those pivot tables to create a bike sales dashboard for stakeholders.

## Cleaning the data:

1. Removed duplicates by selecting the entire dataset and using the 'Remove Duplicates' built-in function in Excel. 
2. Replaced the strings 'S' and 'M' in the Marital Status column with the strings 'Single' and 'Married' respectively.
3. Replaced the strings 'M' and 'F' in the Gender column with the strings 'Male' and 'Female' respectively.
4. Converted the values in the Income column to currency as well as decreased the decimal places to 0 (since the income values are all round numbers anyways).
5. Replaced the string 'Bachelors' with the string "Bachelor's".
6. Added a new column for Age Brackets since the data contains customers ranging from 25-89 y.o which can make it difficult to visualize. Creating age groups will help in creating a clearner visualization. To create the age brackets I used the following formula:

**   =IF(L2>=65, "Elderly 65+",IF(L2>=40, "Middle Age 40-64", IF(L2<40, "Adolescent 0-39", "Invalid")))**

The above formula is a nested IF statement that uses conditions that will return a certain result if true. For example, for **IF(L2<40, "Adolescent 0-39", "Invalid")**, if the age in the cell is less than 40 then replace the cell with the string "Adolescent 0-39". If the conditional statement is false (e.g. the age is NOT below 40) then the cell will be replaced with the string 'Invalid'.

##### Age brackets:
A. Adolescent - for people who are 39 y.o or below.
B. Middle Age - for people who are 40-64 y.o.
C. Elderly - for people who are 65 and above.
