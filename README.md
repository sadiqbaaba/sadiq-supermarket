#Analyze Supermarket Data Across the Country - Company XYZ

Company XYZ owns a supermarket chain across the country. Each major branch located in 3 cities across the country recorded sales information for 3 months, to 

help the company understand sales trends and determine its growth, as the rise of supermarkets competition is seen.

##Project Steps

Step 1 - Loading the Dataset

Import Libraries

import os

import glob

import pandas as pd

os.chdir("/mydir") #Current working directory that contains your dataset and code file

- Use glob to match the pattern "csv"

extension = 'csv'

Combine all the files in the generated list above and export to a CSV

Read the CSV file using pd.read_csv method

Step 2 - Data Exploration.

Import Libraries

import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib.pyplot as plt

%matplotlib inline

plt.style.use('fivethirtyeight')  

import warnings

warnings.filterwarnings('ignore')

Use the head() method to view first few rows of the dataset

Check the number of rows and columns present in the data using the shape attribute.

Generate the names of the columns using the columns attribute.

Statiscal Summary

Below this cell write in few sentences what you can derive from the data statistical summary

Missing values

The isnull, and notna methods can provide a quick overview of the missing data occurence

Data Information

The info() function is used to print a concise summary of a DataFrame

Step 3 - Dealing with DateTime Features

convert to datetime datatype using the to_datetime() method. 

Use to_datetime() to convert the date column to datetime

Check the datatype to confirm if it's in datetime

Repeat the two steps above to the time column

Extract Features from date & time

Extract the Day feature from the Date column, and save to a new Day column

Extract the Month feature from the Date column, and save to a new Month column

Extract the Year feature from the Date column, and save to a new Year column

Extract the Hour feature from the Time column and save to a new Hour column

Pandas provide the nunique() method to get a count of unique values, while the unique() function is used to get unique values of Series object.

From the hours information, determine the numbers of unique hours of sales in the supermarket, and return an array of the hours using the unique() method

Step 4 - Unique Values in Columns

Generate the unique values in the categorical columns (apart from the example - Branch column).

The value_counts() function is used to get a Series containing counts of unique values. For the categorical columns above, generate the count figure of the 

values using the value_counts() method.

Step 5 - Aggregration with GroupBy

Create a groupby object with the "City Column", and aggregation function of sum and mean.

Using the groupby object, display a table that shows the gross income of each city, and determine the city with the highest total gross income.

Step 6 - Data Visualization

Using countplot, determine the branch with the highest sales record. Optional - You can extend this to determine - most used payment method, city with the 

most sales

Explore a countplot for the Payment and City Column

Determine the highest & lowest sold product line, using Countplot

Determine the Payment channel for each branch.

Determine the branch with the lowest rating. This you can determine using abox plot which gives a statistical summary of the plotted features, and you can 

pick out the branch with the lowest rating from the plot

The gender type often affects the kind of products being purchased at the supermarket.

•	Using a catplot() generate visualization for the "product line" on x-axis, quantity on the y-axis, and hue as gender. 

Set the aspect parameter to 4, so can you can effectively space out each product line.

•	Plot the same chart, but Total Column as the y-axis

•	Write a summary of the insights you can pick from this chart.

An interesting insight to explore is the interaction of Unit price on the Quantity of goods purchased. To achieve this:

•	Use the catplot() to plot Product line per unit price, and Product line per Quantity. Set the kind parameter to point 

•	In a new cell, Write a summary of the insights you uncovered

Step 7 - StandOut Section

##Insights

The insights I was able to uncover from analysing the dataset are as follows;

1.	the total number of rows and and columns being 1000,17 respectively.

2.	the city with the highes gross income is Port Harcourt.

3.	the Branch with the highest Sales record is Branch A, lagos.

4.	the most used payment method is epay

5.	the Highest and Lowest Sold product lines, highest in Fashion Accesories and lowest in health and beauty

6.	the city with most sales is Lago

7.	Most used payment channel for each branch is different

8.	Branch B has the lowest rating among the three branches

9.	The closest thing both genders buy is in Electronic Appliances

10.	The farthest thing both genders buy is in Home and Lifestyle


