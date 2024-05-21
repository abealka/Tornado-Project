# Tornado Tracker Project
## Project Overview
1.	Purpose
2.	Sources
3.	Data Cleaning
4.	Data Organization and Analysis 
5.	Data Visualization
6.	Findings

## Purpose
This project showcases my ability to download, clean, analyze, and visualize findings on a public dataset. There are current online trackers and visualizations on tornadoes that are readily available online, which I drew inspiration from. However, all the work presented is my own. 

Questions to explore: 
How many EF5 tornados have there been since 2011? 
What are the states with the most property and crop damages by year? 
What are the months with the most tornadoes on average? 
What states have the highest number of tornados per year overall?

## Data Source
This data was chosen because it has details on property and crop damages, specific locations, tornado lengths, EF scores, casualties, injuries, and times. The bulk data from 1950 onward did not have all of the details I wanted. Therefore, I decided to go back to 2011, when there were several EF5 tornados. *Update: This project was completed prior to April 2024, there are EF5 tornados that have occurred after completion of this project. 

[Raw data from the National Centers for Environmental Information](https://www.ncei.noaa.gov/pub/data/swdi/stormevents/csvfiles/)

## Data Cleaning
Data was cleaned in excel, the CSV individual year datasets were small enough to do so. I ensured each year had consistent formatting to allow unions in BigQuery later on. Of the 51 columns of data only 15 columns were needed: state, event type, county, date and time, indirect and direct deaths, indirect and direct injuries, scale, length, city, damages to crops, and damages to property.

The date time column was split into separate columns for date and military time respectively. 

Damages columns were reformatted from strings (ie. 10K, 10M, 4B) to floats to be used in BigQuery. 

There was an additional scale column added for the EF values, to convert the string values to integers for calculations to be used in Big Query. 

## Data Organization
All queries were run in Big Query 
[Big Query SQL Scripts.](https://github.com/abealka/Tornado-Project/blob/main/tornado_data)

## Data Visualization
[Tableau Dashboard](https://public.tableau.com/views/AverageNumberofTornadosPerYear_17144153500490/Dashboard1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link )

## Findings
All findings are shown in the viz on Tableau.

