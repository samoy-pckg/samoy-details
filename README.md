# samoy-details
# Auto Data cleaner - "samoy"
**samoy** is a Python package for machine learning and data science, built on top of Pandas inbuilt libraries.
This package will be useful for data pre-processing before starting off any machine learning or data science project as it will ease your entire process of data cleaning without much input from the user.
This project is developed in July,2020 by a team of post graduate students and since then many have also contributed.
It is currently maintained by the same team.
## Installation
<b> Dependencies </b>

samoy requires:

- Python (>= 3.6)
- NumPy (>= 1.13.3)
- pandas (>=1.1.0)

<b> User installation </b>

If you already have a working installation of numpy and pandas, the easiest way to install samoy is using `pip`

```
pip install samoy
```

## Package Utilities

In current version of this package it only handles missing,null values and duplicates along with case conversion

<b>Utilities supported: </b>

- Null values handeling : Dropping and imputing(with mean,median as well as custom values)
- Imputing null values with the threshold as mentioned by the user in terms of percentage
- Missing values handeling : Dropping and imputing(with mean,median and LRU)
- Duplicates removal 
- Case conversion like if use wants to convert specific columns or entire column values into either lower or upper case

<b>Name of functions provided in this package: </b>
1. Handeling Null
   - dropnull : This function will drop null in three ways that is dropping all null in the entire dataframe,dropping columns or rows having all nulls and dropping the rows or columns having any of the value as null and return the dataframe after removing null by the method as mentioned by user. By default     it drops all the null if no method is mentioned explicitely.
   - dropnull_th : This function will drop the nulls in those columns where the number of nulls is greater than or equal to the percentage specified by the user and returns dataframe having nulls dropped in those columns where number of null is greater than the percentage(mentioned by user while calling       function) of total number of records in that column.
   - swapnull : This function will replace all the null values with the three different methods like custom method,mean and median and it will return the dataframe having all null values replaced by the method as chosen by the user.By default if nothing is mentioned explicitely,it will impute nulls with the mean value.
   - swapnull_subset : This function will replace all the null values in the columns as specified by the user with the three different methods like custom method,mean and median and it will return the dataframe having all null values replaced  in the selected columns by the method as chosen by the user.By default if nothing is mentioned explicitely,it will impute nulls with the mean value.
2. Handeling Missing
   - swapmissing : This function replace NaN values with mean or median of the specific column. If user mention method as mean or median it will pick it as it is and if user dont want to mention any method then by default mean value to be replaced.
   - swapmissing_subset : This function replace NaN values with mean or median in the specific **numeric** columns only. If user mentions any method like mean or median it will pick it as it is and if user dont want to mention any method then by default missing value will be replaced to mean value.
   - swapmissing_lru : This function will replace the NaN value with last and next value of the same column and if there are many NaN values with start of the column then it will start replacing same with mean of the same column.
   - dropmissing : This function drops missing values from the given data.
   - dropmissing_rows : This function drops rows whose all values are missing.
   - dropmissing_subset : This function drops missing values as well as NaN values from the selcted columns of the dataframe
3. Handeling Duplicates
   - drop_replicatecols : This function will drop duplicate columns  and return the dataframe after dropping the columns having same name(names are also typographically matched with respect to upper or lower case).
   - drop_replicates : This function drops duplicate rows that are present in enitre column of dataframe or within the subset of columns as specifies by users.
4. Case conversion
   - altercase : This function is usually to convert the content of dataframe either in lower case or upper case.
   - altercase_subset : This function is usually to convert the content of only selected columns either in lower case or upper case and returns dataframe having the content of mentioned columns either in lower or upper case.

<b>Details of each functions </b>

To know the detailed summary of each function along with its parameters and a demo example to use it,please use command `help(name_of_function)`


## Contact Us:

Email: samoyapi@gmail.com
