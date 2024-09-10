<a id="readme-top"></a>

## Project Goal
The goal of this project is to understand SQL fundamentals, the exploratory data analysis (EDA) process in Python using various libraries, and the functionality of Tableau for converting datasets into meaningful visualizations that help inform business decisions.

We explored several datasets and selected one that best suited answering key business questions. This process helped in understanding dataset behavior, structure, and data types. I chose the Real Estate dataset for this project.

The primary objective is to identify price differences for properties listed by different agencies. 

Using either regression to predict prices or classification to categorize properties based on attributes, the project aims to offer data-driven recommendations to real estate professionals. 

The final deliverable will be a dashboard showcasing neighborhood and property options tailored to a client's budget and other specific needs.


## Project Description
This project addresses the challenge of recommending relevant real estate listings to clients based on their budgets and preferences. The analysis focuses on predicting sales prices and estimating living area sizes.

By analyzing and comparing listings from different agencies, the model will determine whether listings represent the same property and identify price differences. Additionally, it will classify properties based on features such as living area size, number of rooms, and bedrooms. 

This will enable real estate professionals to streamline their recommendation process and enhance client service through an interactive dashboard.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Process
### Analyze the Dataset (Dataset: Real Estate)
Please  refer to the below link to the original documents

https://drive.google.com/file/d/18GQ1LM09oLGDLhihUKd4HANgoxrfEEUU/view?usp=sharing  

Note – Please refer to the jyputer Notebook – Real_Estate_Dataset EDA.ipynb for the python code in the folder called – Data_files. 

Step 01 – Load the original datasets, testListing.csv and trainListing.csv

The main focus was on the testListings and trainListings files. Both files contained the same columns, so concatenated them to create a single, combined dataset. The columns are as follows:id – identifications of the property

* sourceId – identification of the agency
* locationId – location identification of the property
* price – sale/ rent price of the property
* rooms – some agencies use this as a total number of rooms
* bedrooms – number of bedrooms
* bathrooms – number of bathrooms
* totalArea – size of the full buildup area
* livingArea – size of the living area
* plotArea – size of the plot area
* terraceArea – size of the terrace area
* title – property titles, text area
* description – property description, text area
* feature – property features list in plain text
* latitude & longitude – property coordinate, present in rear case
* thumbnails - List of thumbnail IDs.

Step 02 – Check the number of null values for each column and remove unwanted and unclear columns. ('title', 'description', 'features', 'latitude', 'longitude', 'thumbnails') – File1_concat_remove_columns_listings.xlsx. 

Step 03 – Define the unique column for the data analysis purpose – “id” is the unique column. Remove non-numeric values from id column and source should be mandatory – File2_concat_remove_columns_rows.xlsx

Step 04 – Remove rows where price values are empty – File3_concat_remove_columns_rows_price.xlsxBased on the null values report, I removed columns - Number of executions (Amnesty International) because it contained 7987 null values. And saved as an excel file, ‘death_cause_column_removed.xlsx’

Step 05 – This analysis based on Houses and Apartments. From the file need to filter the houses and apartments. (typeId: 1,2,3,4,5,6,7,9,10,11,12) – File4_houses_apartments.xlsx

Step 06 – Remove columns – rooms, livingArea, plotArea, terraceArea because those values difficult to understand and very contradictive – File5_houses_apartments_remove_columns.xlsx

Step 07 – Assuming there should be at least a bathroom or bedroom in a house or apartments. Removed zero bathrooms and bedrooms from houses and apartments and saved it in an excel, File6_houses_apartments_remove_zeros.xlsx

Step 08 – Make assumption as maximum number of bedrooms and bathrooms a house or apartment could have is 10 (create a threshold as 10) and remove rows which have more than 10 bedrooms and bathrooms – File7_houses_apartments_less10_bedrooms_bathrooms.xlsx

Step 09 - Make assumption as maximum total area a house or apartment could have is 999 (threshold as 999) and remove rows which have more than 999 total area – File8_houses_apartments_remove_totalarea.xlsx

Step 10 - Every property should have a location so remove rows which are location is empty – File9_houses_apartments_empty_locations.xlsx

Step 11 - Make necessary changes and create the final version of the dataset – File10_houses_apartments_final_version.xlsx

Step 12 - Data Visualization

### Assumptions & Decisions 

1. Decided to move forward with the houses and apartments. Excluded - invesmemts, plots and other types
2. Concatenated both files, testListings.csv and trainListings.csv because there were nothong metiong about why the dataset contains two files with same columnns.
3. After checking the duplicate rows, realizes id is the primaty and unique columns for the dataset
4. Each property should have an agent and locations.
5. Assumed maximum number of bedrooms and bathrooms for a house or apartment is 10.
6. Assumed maximum total area for a house or apartment is 999.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Results
### Visualizations – 
1.	Number of residences - it gives how many houes and apartments in selected location/s
2.	Average prices based on the locations - optiont to select the location/s and type of the residence (house or apartment) and graph will give you the average price
3.	Price variation based on the bedrooms, bathrooms and total area - option to select the location/s, you see the how price vary with the number of bedrooms, bathrooms and total area
4.	Residence prices - optiont to select the location/s and type of the residence (house or apartment). And you will be able to filter the number of bedrooms, bathrooms and total area as a rnage. Graph will give you the numbers
5.	Price based on the # of the bathrooms of the residence with the trend line
6.	Price based on the # of the bedrooms of the residence with the trend line
7.	Price based on the # of the total area of the residence with the trend line
8.	Dashboard - Real Estate Ingihts - Houses and Apartments

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Challenges 
#### 01.	Data Cleaning and Preparation:

Handling missing or inconsistent data, such as mixed-up few columns and null values in the dataset.
Standardizing the id column which contained a mix of strings, null values.
With large number of data analysing data is difficult. Can't come up with accurate results because there are lots of unusal values.

#### 02.	Feature Selection:

Identifying the most important features out of the 36 available columns.
Deciding which causes of death to focus on and which features provided the most relevant insights for global or country-level analysis.

#### 03.	Visualization Challenges:

Designing effective visualizations that convey the key insights while dealing with a large number of variables.
Building interactive and meaningful dashboards that included maps, forecasting, clustering, and other analytical visuals.

#### 04.	Technical Issues:

Learning and applying Tableau’s calculated fields, filters, and custom visualizations.
Managing performance issues due to the size of the dataset, especially when creating complex visualizations.

#### 05.	Dashboard Design:

Iterating on the dashboard design to ensure it was user-friendly, informative, and answered the key questions identified during the analysis.
Deciding on which visualizations to include and how to layout the dashboard effectively.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
