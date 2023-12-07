# Project_1

# The objective of our project is to identify patterns and trends in airfare pricing for specific destinations based on their carrier.
 Analyze trends over time (quarters) for selected city pairs.
 Examine how the markets have evolved, identifying any patterns or significant changes.
 Explore variations in average fares across different cities within city pairs.
 Identify cities with consistently higher or lower average fares.
 Investigate factors contributing to increases or decreases in average fares.
 Explore datasets related to increased and decreased average fares for insights.
 Examine the variability in fare prices for specific routes.
 Identify routes with significant fluctuations in fares, providing insights into pricing dynamics.
 Investigate seasonal patterns in airfares and passenger numbers by analyzing quarterly variations.
 Understand how prices and demand change throughout the year.

# The approah 
  Get data from the Domestic Airline Consumer Airfare Report from the United States Department of Transportation.
  This data is available to the public and contains data regarding fares and carriers traveling domestic routes across the country for the different quarters of the year. 


# Data Cleaning
Utilized Table 1a for all of our research questions since it had the most detailed information 
Read in the Multi_City_Airport_Markets.csv
Renamed some of the column names for understanding purposes
used the .loc function to fill the geocode values in the places where there was NAN
created a clean dataframe that includes only the 3 specific routes that we wanted to analyze (Los Angeles to Seattle,WA) and (Los Angeles to Washington, DC) and LA to Tampa, Florida

# ..............................................................................................................................


# Research Question 1







# Research Question 2






# Research Question 3







# Research Question 4
wanted to look at fare variability so from the clean dataframe
The columns of interest are Quarter, Arrival_city, and Fare
Used the .groupby function and grouped the dataframe by the quarter and the Arrival_city and then calculated the maximum value on the fare column for each of the 2 years that we looked at
Then we also used the groupby function to group the quarter and Arrival_city and then calculated the minimum fare on the fare column

Then I was able to subtract the maximum fare column from the 2017 groupby from the minimum fare column in the 2017 groupby to get the difference in the fare from each route 

was able to conclude that the most price variable route is from Los Angeles to Washington DC






# Research Question 5




