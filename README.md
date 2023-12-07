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





#.................................................................................

# Research Question 2
The goal of this analysis is to understand how average fares vary across different arrival cities for flights departing from Los Angeles, CA (Metropolitan Area) during each quarter of the year 2018. By grouping the data based on the quarter and arrival city, we aim to identify patterns and trends in airfare pricing for specific destinations.

Key Steps in the Analysis:

Data Preparation:

Extract and filter the dataset to include only flights departing from Los Angeles, CA, with specific arrival cities (Washington, DC, Tampa, FL, Seattle, WA).
Ensure that the dataset covers the entire year 2018.
Grouping and Aggregation:

Group the data by both quarter and arrival city.
Calculate the average fare for each group, providing insights into the typical cost of flights to different destinations during each quarter.
Visualization:

Use a bar plot to visually represent the average fare for each arrival city in each quarter. This allows for easy comparison of fare variations across destinations and over time.
Interpretation:

Analyze the plotted results to identify any notable trends, seasonal patterns, or differences in average fares between the specified arrival cities.
Look for insights that could help in understanding the factors influencing airfare pricing for these specific routes.
By conducting this analysis, we aim to provide stakeholders with a clear and concise overview of how average fares vary across different arrival cities from Los Angeles throughout the year 2018. The results may contribute valuable information for decision-making in the airline industry or for travelers considering specific routes.

#..................................................................................

# Research Question 3
This question focus on analyze the impact of the distance between airports, and the number of passengers an specifict airline routes on the fares.

From the clean DataFrame, create a new DataFrame with only columns "Year","quarter", "Departure_city", "Arrival_city", "Non_stop_Miles", "passengers", "fare". After that, plot the scatter plot with x-axis is the number of passengers and the y-axis is the fares. Plot the regression line and calculate the correlation number between the number of passengers and fares. Similar to previous scatter plot and line plot, plot the scatter plot with x-axis is the distance (miles) and the y-axis is the fares. Plot the regression line and calculate the correlation number between the distance and fares.

Then analyze the relationship between the number of passengers versus fares and the distance between airports versus fares based on their correlation number.

#................................................................................................
# Research Question 4
wanted to look at fare variability so from the clean dataframe
The columns of interest are Quarter, Arrival_city, and Fare
Used the .groupby function and grouped the dataframe by the quarter and the Arrival_city and then calculated the maximum value on the fare column for each of the 2 years that we looked at
Then we also used the groupby function to group the quarter and Arrival_city and then calculated the minimum fare on the fare column

Then I was able to subtract the maximum fare column from the 2017 groupby from the minimum fare column in the 2017 groupby to get the difference in the fare from each route 

was able to conclude that the most price variable route is from Los Angeles to Washington DC

#....................................................................................

# Research Question 5
The goal of this research question is to understand the seasonal patterns in air fares and passenger numbers.

We tooks the cleaned up data and filtered it using loc to reduce it to the cities of interest. Departure = LA and arrival= Tampa, Seattle, Washington DC

We Groupe the filtered data using Year, Arrival City and quarter and caluclated the means for fare, distance and passengers. Then we calcualted the average fare per mile

The using this data, we made the plots to see Passenger information vs Quarters and Fare vs Quareters. Made the line plots for each city and analyzed it to see the patterns.

We were able to make observations and make recommendations based on these plots.

Then to show the correlation between avg fare per mile vs distance, did a geo map using the geoapify APIs. Got the latitude/longitude for each cities and then did 3 hvplots - one for the points for each city and 2 for labels with distance and city name. Super imposed them together to get the final map chart.



