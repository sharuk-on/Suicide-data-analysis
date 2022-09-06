# In-depth analysis on Suicide in India (2001-2014) [Blog post]()
## Data cleaning using python
### About Primary dataset:
The datasets collected for this project represents 5 different aspects of the suicide victims, they are.

- **Cause/Circumstances of the suicide**
-	**Educational status of the victim**
-	**Professional profile of the victim**
-	**Marital status of the victim**
-	**Means adopted by the victim**

There are 15 primary dataset i.e, 3 for each aspects based on the year (2001-2012), (2013) and (2014).

The dataset for 2001-2012 and 2013 are similar in all the aspects like naming conventions, data categorizations etc., whereas the 2014 dataset is vastly different in every aspect.

Now the task at hand is to **clean**, **combine**, **wrangle**, **standardize** data.

Let’s see the data cleaning process that used to clean all the 5 aspects of the datasets.

## Data cleaning process
### Removing unwanted columns
- Every 2014 dataset contains columns that are not present in other datasets, like the column for “Transgender” and “Total”. So, it had to be removed.

### Standardizing column names and concatenating datasets.
- The column names are different for every dataset, in order to combine these three datasets, we need to standardize column names first. Then we use “concat” function combine all three datasets.

### Cleaning “State/UT” column
- As mentioned already, the naming conventions between datasets are vastly different. 
- For example, “Andaman and Nicobar” is also named as “A & N islands” and “A and N islands”. Using function to standardize all names of the State/UT.

### Removing unwanted datapoints in “States/UT” column
- “State/UT” column contains some datapoints that represent aggregate value like “Total (all India)”, “Total (states)” and “Total (uts)”. Since we don’t want aggregate value among the data, it had to be removed. 
### Cleaning “[respective aspect]” column
- As mentioned, we have 5 different aspects and each one of them required specific changes.
- Again, the naming conventions are vastly different which needs to standardized using function.
### Removing unwanted datapoints in “[respective aspect]” column
- Again, there are some datapoints that represent aggregate value. They are promptly removed.

### Creating new column
- This new column values will represent whether the region in “State/UT” column is “State” or “UT”. 
### Rearranging and renaming columns, sorting values and resetting index
- We are rearranging column and sorting values based on “State/UT” and “Year”.
- Then we reset index and renaming columns.

***All 5 facets of dataset went through the same data cleaning process.*** 

### Secondary Dataset
- These census dataset are used to calculate per capita victims.
