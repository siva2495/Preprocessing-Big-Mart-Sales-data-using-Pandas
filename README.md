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
