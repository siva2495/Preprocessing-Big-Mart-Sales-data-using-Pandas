# Preprocessing-Big-Mart-Sales-data-using-Pandas
## Preprocessing Subsetting Modifying DF

### 1. Overview of Subsetting in Pandas:

### TABLE OF CONTENTS

•	What is an index?

•	How to subset first N rows based on their position index?

•	Can we change the index?

•	Will the index be always numeric?

•	How to subset the data based on a label of the index?

•	Can we reset the index?

•	How to subset the data based on a value of a column?

In this note book, we are going to use the big mart sales data for this analysis.

#### What is Index?
•	You can see the index object by DataFrame.index.

#### How to subset first N rows based on their position index?
•	You can subset N rows by DataFrame.head () function passing index number into the parenthesis.

#### Can we change the Index?
The answer is Yes, We can change the index by using following function DataFrame.set_index()

Set another column of the dataframe as the index. We will use the set_index function. You can read more about here:
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.set_index.html'

##### Will the index be always Numeric?
No, We can also have categorical variables as the index of a dataframe.

#### HOW TO SUBSET THE DATA BASED ON THE LABEL OF THE INDEX?
•	We can subset the data based on the label of the index using the loc function.

#### What if we want to change the index back to positional?
CAN WE RESET THE INDEX?
Yes, we can reset the index. Let's see how? We will use the reset_index function. You can read more about here: 
https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.reset_index.html


### 2.	Subsetting: Position Based

### TABLE OF CONTENTS

•	How to view the top and bottom rows of the data?

•	How to select rows in a particular range?

•	How to select the rows by position?

•	How to select the specific rows and columns from the data using their position?

#### How to view the top and bottom rows of the data?

•	Use head function to view top n rows.

•	Use tail function to view bottom n rows.

#### How to select rows in a particular range?
•	Use DataFrame[ ] to select particular range.

#### How to select the rows by position?
•	When we are using iloc, we need to specify the rows and columns by their position.

#### How to select the specific rows and columns from the data using their position?
•	In the iloc function pass the first list as the order of rows by their index and pass the second list as the order of columns.

### 3. Subsetting: Label Based 

### TABLE OF CONTENTS
•	How to select rows using the label of the index?

•	Difference between loc and iloc

#### HOW TO SELECT ROWS USING THE LABEL OF THE INDEX?¶
•	We can subset the data based on the label of the index using the loc function.

#### HOW TO SELECT ROWS & COLUMNS USING THE LABEL OF THE INDEX?
•	We can use same loc function to subset row and columns by giving their attributes.

#### DIFFERENCE BETWEEN LOC AND ILOC
•	When we try to slice the dataframe using the loc function on range(2 to 4) it first finds out the index with a label 2 and goes till it finds the index with a label 4.

•	On the other hand, when we try to silce the dataframe using the iloc function on range(2 to 4) it starts with the starting point index 2 and goes till end point - 1 which 
is 3.

•	In other words when we tried to slice the dataframe using the loc function it finds out the name of start and end point and slice the data whereas iloc still gives the 2nd and 3rd value of the dataframe.

### 4.	Subsetting: Value Based
Here we can see
  •	How to select rows based on condition
  
  •	How to select rows based on multiple conditions
  
  •	How to select specific columns from a data

  •	How to select rows based on a condition and view only the specific columms

  •	How to select the columns with specific data types

#### HOW TO SELECT ROWS BASED ON MULTIPLE CONDITIONS?
•	When passing multiple conditions make sure that you put each of the condition in a parenthesis ().

#### HOW TO FILTER FOR A LIST OF VALUES?
If you want to filter for a list of values from a column then instead of writing multiple conditions use the isin function.

#### HOW TO SELECT SPECIFIC COLUMNS FROM A DATA?
•	You just need to pass a list of columns that you need.

##### HOW TO SELECT ROWS BASED ON A CONDITION AND VIEW ONLY THE SPECIFIC COLUMMS?
Using Square brackets

#### df[] VS df.loc[] WHEN TO USE WHICH?
•	df.loc[] provides simpler syntax over df[]

•	Both have similar performance in terms of execution time

•	df.loc[] also works with label based subsetting

•	df[] sometimes has unwanted behavior, hence as a good practice it is recommended to use df.loc[].

Read here for more info: https://stackoverflow.com/a/38886211

### 5. Modifying Data
Here we can see

•	How to impute the missing values in any column

•	How to update the values of a column with a new mapping

•	How to create a new column by modifying the existing column

•	How to convert categorical variables into numerical

#### HOW TO IMPUTE THE MISSING VALUES USING LOC IN ANY COLUMN?
Check the columns with null values.
First, we will check the number of missing values in each of the column. Use the function isna().sum().

use the fillna function to impute the missing values.
•	fillna function is another way to impute the missing values. Use the parameter inplace=True to store the results in the dataframe.

#### HOW TO CONVERT CATEGORICAL VARIABLES INTO NUMERICAL?
Most of the machine learning algorithms do not take categorical variables so we need to convert them into numerical ones. In pandas, we have one such function get_dummies which will help us in doing such tasks. It will create a binary column for each of the categories.
 
This is also known as One Hot Encoding. You will learn more encoding techniques in the data pre-processing module.
