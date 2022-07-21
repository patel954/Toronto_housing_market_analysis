# Group 2 – Project 1: Real Estate investment options in Toronto

## Background

The city of Toronto real estate prices have increased greatly in the last 5 years. This increase may be different among its neighborhoods.
 It is said that investing in real  estate in Toronto is always a good investment; however, this investment and potential 
gains may differ among the neighborhoods. When investing one must keep in mind lot of factors such as area demographics, price history in the last 5 yrs, year built and commute to name a few. The most important aspect is the price graph which would determine how safe is the investment. Some areas in Toronto may not have a price gain at all. Depending on different locations there maybe a price decrease based on crime rate and the age of the structure. Analysis on price not only helps us decide best locations to invest in but also eliminates some hidden factors discussed earlier. Now we must keep in mind that the past analysis will not always be ideal. The current market is really unpredictable with banks raising their interest rates and the property increasing in value more than 150% from the past 10 yrs. Atificial inflation of house prices along with fluctuating bank interest rates make it really hard to make a proper decesion. Furthurmore there is crisis everywhere with corona virus on one end and the natural disasters on the other. Prices for raw material have sky roketed and most of the material is not even available or has really long timelines. Based on the current market analysis it would almost be impossible to make an investment wthout blocking your funds with long timelines.The best option nowadays is to target good investment areas with stable prices. A good price trend or analysis is the key in making that happen. The reason we choose this project is to make it easier for an invetor who is looking to make a safe investment in current market. Our analysis would help an investor make a safe and informed decesion based on price data and its evaluation for the past 5 yrs. 

In this project, the group will complete an analysis of the development of the real estate 
prices of the 15 neighborhoods of the city of Toronto with the purpose of identifying the 
best neighborhoods for investment opportunities.

The group will accomplish two main tasks:

### 1. Data preparation: Complete a research of the data available for the project, 
including the use of APIs; and define the data for the project Review and clean 
the data to have csv files
### 2. Data analysis: Analyze the data to identify the real estate price trends and 
projections and develop a report of observation and conclusions

### 1. Data preparation:

Prepare the data in a csv file with the real estate prices for the last 5 years for detached  and apartment residences in Toronto and its neighborhoods:

![ Real Estate Prices TO](C01_C15_Clean_df.csv)

Prepare the data in a csv format file with the geographical longitude and latitude 
information for the 15 neighborhoods of Toronto
long_lat_TO.csv

### Import the functions

Import pandas as pd
import os
import requests
import pandas as pd
from dotenv import load_dotenv
import alpaca_trade_api as tradeapi
from pathlib import Path
import seaborn as sns
import numpy as np 
### Prepare the dataframe for the realestate prices in Toronto
EXAMPLE CODE FOR C04 TO C06
C04_C06_df = pd.read_csv(Path('../Toronto_housing_market_analysis/Data/C01_C15_Clean_df.csv'))
C04_C06_df = C04_C06_df.drop(["CompIndex","SFDetachIndex","SFAttachIndex","ApartIndex", "SFAttachBenchmark","SFAttachYoYChange", "THouseIndex", "THouseBenchmark", "THouseYoYChange"], axis=1)
C04_C06_df.head()
C04_C06_df.set_index('Date', inplace=True)
C04_C06_df
C04_C06_df = C04_C06_df.iloc[2346:3312]
C04_C06_df
C04_C06_df.set_index('Date', inplace=True)
C04_C06_df
C04_C06_df.to_csv("C04_C06_df.csv")

display(C04_C06_df.head())
display(C04_C06_df.tail())
### Calculate and plot the real estate prices for the last 5 years: 

Toronto - Use the groupby function to group the data by year. 
Aggregate the results by the mean of the groups – 

What are the real estate price trends for Toronto composite 
and for the detached and apartment over the 5 years 
period?
Steady increase in price 

### Calculate and plot the real estate prices for the last 5 years By  neighborhood - Use the groupby function to group the data by year. Aggregate the results by the mean of the neighborhoods
What are the real estate price trends for Toronto and neighborhoods over the 5 years period? Increase 
Which neighborhoods have the largest price increase, and which have the lowest price increase?Highest c12, lowest C11
Any neighborhood(s) that experienced a real state price reduction? No

### Complete a Projection for the next 5 years; for Toronto and by neighborhoods. Including a  Montecarlo simulation for the projected average prices by neighborhood and a Plot to compare the projections for Toronto and its neighborhoods
What is the projected trend for Toronto and its 
neighborhoods for the next 5 years? 
For composite vs other type of residences Steady Increase Only 

### Build an interactive GeoViz map that shows the real estate prices (latest point in time).  Concatenate the two dataframes(Neighborhoods real estate prices annual mean and  the neighborhoods Lat/Long coordinates and create a Geoviews 
hvplot map
Which are the neighborhoods with the highest prices in 
Toronto - composite? C12
Which are the neighborhoods with the highest prices in 
Toronto  detached houses? C12
Which are the neighborhoods with the highest prices in 
Toronto  appartments? C12 & C02 

## Conclusion
What insights can you derive about the decision of investing 
in real estate in Toronto? What are your choices (5 top 
combination of neighborhoods and type of residence ) for 
investing in real state? C11, C01, C15,C06 & C13
How did you derive to your recommendation? # Toronto_housing_market_analysis
Based on our findings by cleaning up the data , projections and maps we have discovered that the top rated neighborhood is C12. Other than C12 top 5 neighborhoods include C11, C01, C15,C06 & C13. 