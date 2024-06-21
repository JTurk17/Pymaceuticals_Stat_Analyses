# Pymaceuticals_Stat_Analyses

Background:
You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

For this project I had to use several outside sources throughout the code that are documented below. In addition to the url for the site where I got the information I include a brief bullet point on how and where I used the code. 

Here is a summary breakdown of what the code achieves:

* Prepare the data
  - Run the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.
  - Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.
  - Display the updated number of unique mice IDs.
 
* Generate Summary Statistics
  - Create a DataFrame of summary statistics.
    - A row for each drug regimen.
    - A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.
   
* Create Bar Charts and Pie Charts
  - Generate two bar charts. Both charts are identical and show the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.
    - Create the first bar chart with the Pandas DataFrame.plot() method.
    - Create the second bar chart with Matplotlib's pyplot methods.
  - Generate two pie charts. Both charts are identical and show the distribution of female versus male mice in the study.
    - Create the first pie chart with the Pandas DataFrame.plot() method.
    - Create the second pie chart with Matplotlib's pyplot methods.
   
* Calculate Quartiles, Find Outliers, and Create a Box Plot
  - Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens.
  - Using Matplotlib, generate a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.
 
* Create a Line Plot and Scatter Plot
  - Select a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.
  - Generate a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.
 
* Calculate Correlation and Regression
  - Calculate the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.
  - Plot the linear regression model on top of the previous scatter plot.


For this project I had to use several outside sources throughout the code that are documented below. In addition to the url for the site where I got the information I include a brief bullet point on how and where I used the code.

1. https://saturncloud.io/blog/how-to-find-all-duplicate-rows-in-a-pandas-dataframe/#:~:text=To%20find%20duplicate%20rows%20in%20a%20pandas%20dataframe%2C%20we%20can,get%20all%20the%20duplicate%20rows.
  - I used this in line 3 with .loc to find the duplicated data in my DataFrame.

2. https://www.geeksforgeeks.org/python-delete-rows-columns-from-dataframe-using-pandas-drop/
  - I used this to assist with dropping mouse g989 from the Dataframe in line 5.

3. https://www.geeksforgeeks.org/grouping-and-aggregating-with-pandas/
  - I used this in line 8 to assist with using the .agg function.

4. https://www.geeksforgeeks.org/how-to-rotate-x-axis-tick-label-text-in-matplotlib/
  - I used this to assist with rotating the x labels in line 10. 
