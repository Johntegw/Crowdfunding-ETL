# Crowdfunding-ETL
Background
Independent Funding loves what you and Britta have done with both the crowdfunding ETL project and the SQL data analysis. But, you still have more to do! The company has just received a new dataset that contains information about the backers who’ve pledged to the live projects. And, Independent Funding wants you and Britta to perform both an ETL process on this dataset and a data analysis by using SQL queries.

In this Challenge, you’ll use Python, Pandas, and Jupyter notebooks to do the extract and transform phases. Specifically, you’ll extract and transform the backers’ contact information from a CSV file to create a DataFrame that will be exported as a CSV file. You'll then do the load phase. Specifically, you’ll use the dataset to create an ERD and a table schema for creating a new table in the crowdfunding_db database. And, you’ll upload the CSV file that contains the backers’ information into this table. Finally, you’ll perform a data analysis on the crowdfunding_db database by using SQL queries.

What You're Creating
This new assignment consists of four technical analysis deliverables. You will submit the following:

Deliverable 1: Extract Data
Deliverable 2: Transform and Clean Data
Deliverable 3: Create an ERD and Table Schema, and Load Data
Deliverable 4: SQL Analysis
Instructions
Deliverable 1: Extract Data
Using your knowledge of Python, Pandas, and the extract and transform phases of ETL, you’ll extract the raw data and add it to a DataFrame for the transform phase.

Download the backer_info.csv and Extract-Transform_starter_code.ipynb files into your Crowdfunding-ETL folder. Then rename the Extract-Transform_starter_code.ipynb file to Extract-Transform_final_code.ipynb.

Import the backer_info.csv file into a DataFrame.

Note that for this deliverable you have two options for extracting the data: use Python dictionary methods or use regular expressions. Choose your option.

To use use Python dictionary methods, complete the following steps:

Iterate through the DataFrame, and convert each row to a dictionary.

Iterate through each dictionary, and do the following:

Extract the dictionary values from the keys by using Python list comprehensions.
Add the values for each row to a new list.
To use regular expressions, complete the following step:

Extract the "backer_id", "cf_id", "name", and "email" string values.

If you’d like a hint for extracting the alphanumeric "backer_id" and the numeric "cf_id" identification numbers, that’s totally okay. If not, that’s great too. You can always revisit this later if you change your mind.

HINT
Create a new DataFrame with the retrieved data.

Confirm that your DataFrame matches the following image:

A screenshot depicts the first 10 rows of the DataFrame.

In the preceding image, notice that the DataFrame has "backer_id", "cf_id", "name", and "email" columns. And, each column contains the extracted data from the backer_info.csv file.

Deliverable 2: Transform and Clean Data
Using your knowledge of Python, Pandas, and data cleaning strategies, you’ll transform the data via formatting, splitting, converting data types, and restructuring to create a DataFrame that can be loaded into a postgreSQL database as a CSV file.

Continuing to use the Extract-Transform_final_code.ipynb file, check the data types of the columns, and convert the "cf_id" column to int64 if necessary.

Split the names in the "name" column into first and last names, and add them to "first_name" and the "last_name" column, respectively, in the DataFrame.

Drop the "name" column in the DataFrame.

Reorder the columns so that your DataFrame matches the following image:

A screenshot depicts the final DataFrame.

In the preceding image, notice that the DataFrame has the columns in the following order: "backer_id", "cf_id", "first_name", "last_name" and "email".

Export the DataFrame as backers.csv.

Deliverable 3: Create an ERD and a Table Schema and Load the Data
Using the ERD that you created in this module, you’ll create a backers table that has primary and foreign keys based on the summary information about the backers.csv dataset. You'll then export the updated database schema as a PostgreSQL file and use it to create the backers table in the crowdfunding_db database. Finally, you'll use pgAdmin to upload the backers.csv file into the backers table.

Using the information from the backers.csv file, open the crowdfunding_db ERD that you created in this module and create a backers table.

Make sure that each column has the appropriate data type, that the table has a primary and a foreign key, and that the foreign key references the relevant table.
Save the crowdfunding relationship diagram as crowdfunding_db_relationships.png and the updated schema as a PostgreSQL file named crowdfunding_db_schema.sql.

Using the crowdfunding_db_schema.sql PostgreSQL file, copy the schema for the backers table and the ALTER TABLE statement to add the foreign key constraint, paste them in the pgAdmin query editor, and then run the query.

Refresh your schema in the crowdfunding_db database to confirm that the backers table was created.

Upload the backers.csv file into the backers table.

To check the import, enter the following in the query editor, and then run the query:

SELECT * FROM backers;

Confirm that the first 10 rows of the backers table match the following image:

A screenshot depicts the first 10 rows of the backers table in postgreSQL.

In the preceding image, notice that the backers table should mirror the CSV file.

Save crowdfunding_db_relationships.png and crowdfunding_db_schema.sql in your Crowdfunding-ETL GitHub repository.

Deliverable 4: SQL Analysis
Download the ETL_SQL_starter_code.sql file, and rename it to crowdfunding_SQL_Analysis.sql.

Write a SQL query that retrieves the number of backer_counts in descending order for each “cf_id” for all the "live" campaigns.

Write a SQL query that uses the backers table to confirm the results from Step 2.

You and Britta receive notification from her boss, who wants to send an email to each contact of every live campaign to inform them of how much of the goal remains. To allow them to do so, complete the following steps:

Write a SQL query that creates a new table named email_contacts_remaining_goal_amount that contains the first name of each contact, the last name, the email address, and the remaining goal amount (as "Remaining Goal Amount") in descending order for each live campaign.

Confirm that the table matches the following image:

A screenshot depicts the first 10 rows of the table.

In the preceding image, notice that the "email_contacts_remaining_goal_amount" contains the remaining goal amount for the live campaigns in descending order, and the first and last name, and email address of each contact .

Export the table as email_contacts_remaining_goal_amount.csv.

Britta informs you that her boss also wants to send an email to each backer to let them know how much of the goal remains for each live campaign that they’ve pledged. To allow them to do so, complete the following steps:

Write a SQL query that creates a new table named email_backers_remaining_goal_amount that contains the email addresses of the backers, the first and the last name of each backer, the cf_id, the company name, the description, the end date of the campaign, and the remaining amount of the campaign goal as "Left of Goal". Sort the table by the last name of each backer, in descending order.

Confirm that your table matches the following image:

A screenshot depicts the first 10 rows of the table.

Export the table as email_backers_remaining_goal_amount.csv.

Add your queries to the crowdfunding_SQL_Analysis.sql file, and then save the file in your Crowdfunding-ETL GitHub repository.

SUMMARY 
THis project allowed us to sucessfully download and import files into a SQL data base and also to create tables within the SQL environment as well. Some aspects of the code, I had to review on line help to correct for importing files and syntax errors. Overall, I think the challenged turned out good. 
