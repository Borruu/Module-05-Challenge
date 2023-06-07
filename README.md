# Pharmaceutical technical report using Matplotlib and Pandas
The purpose of this project is to demonstrate how Pandas and Matplotlib can be used for technical reporting. 

Mock data is used to simulate a clinical study of cancer treatments. 
## Scenario
<!-- You've just joined Pymaceuticals, Inc., a new pharmaceutical company that specialises in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. -->
<!-- As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study.  -->
Pharmaceutical company requires report on their most recent animal study.

In this study, 249 mice who were identified with SCC tumours received treatment with a range of drug regimens. Over the course of 45 days, tumour development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

**Deliverables:**
1. Generate all of the tables and figures needed for the technical report of the clinical study.
2. Provide a top-level summary of the study results.

<!-- The executive team has tasked you with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results. -->

## Files
1. Source data:
   - [Mouse_metadata.csv](Mouse_metadata.csv)
   - [Study_results.csv](Study_results.csv)
2. Script:
   - [MySolution.ipynb](MySolution.ipynb)
   - [pymaceuticals_starter.ipynb](pymaceuticals_starter.ipynb)

## Steps

- Prepare the data.
- Generate summary statistics.
- Create bar charts and pie charts.
- Calculate quartiles, find outliers, and create a box plot.
- Create a line plot and a scatter plot.
- Calculate correlation and regression.
- Submit final analysis.

### Prepare the Data
1. Run the provided package dependency and data imports, and then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.
2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining steps.
3. Display the updated number of unique mice IDs.

### Generate Summary Statistics
Create a DataFrame of summary statistics, including:
- A row for each drug regimen. These regimen names should be contained in the index column.
- A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumour volume.

### Create Bar Charts and Pie Charts
1. Generate two bar charts. Both charts should be identical and show the total number of time points for all mice tested for each drug regimen throughout the study.
   - Create the first bar chart with the Pandas `DataFrame.plot()` method.
   - Create the second bar chart with Matplotlib's `pyplot` methods.

2. Generate two pie charts. Both charts should be identical and show the distribution of female versus male mice in the study.
   - Create the first pie chart with the Pandas `DataFrame.plot()` method.
   - Create the second pie chart with Matplotlib's `pyplo`t methods.

### Calculate Quartiles, Find Outliers, and Create a Box Plot
1. Calculate the final tumour volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens. Use the following substeps:
   - Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.
   - Create a list that holds the treatment names as well as a second, empty list to hold the tumour volume data.
   - Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumour volumes for each drug to the empty list.
   - Determine outliers by using the upper and lower bounds, and then print the results.

2. Using Matplotlib, generate a box plot that shows the distribution of the final tumour volume for all the mice in each treatment group. Highlight any potential outliers in the plot by changing their color and style.

### Create a Line Plot and a Scatter Plot
1. Select a mouse that was treated with Capomulin, and generate a line plot of tumour volume versus time point for that mouse.
2. Generate a scatter plot of tumour volume versus mouse weight for the Capomulin treatment regimen.

### Calculate Correlation and Regression
1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumour volume for the Capomulin treatment.
2. Plot the linear regression model on top of the previous scatter plot.

## References
Data generated by **Mockaroo** https://mockaroo.com/, LLC (2022). Realistic Data Generator.
