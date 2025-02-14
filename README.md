# TORONTO VEHICLE COLLISIONS ANALYSIS
 <p align="Left">
  <img src="https://github.com/user-attachments/assets/5e9916e0-7dea-4f34-b5e6-86e71a69ddb8" width="900" height="500" alt="Alt text">
   </p>




## Table of Contents

## 📌 Table of Contents  

1. [Introduction](#OVERVIEW)  
2. [Background & Problem Statement](#BACKGROUND--PROBLEM-STATEMENT)  
3. [Aim](#AIM)
4. [Tech Stack](#TECH-STACK)
5. [Data](#DATA)  
6. [Project Outcomes & Insights](#PROJECT-OUTCOMES-AND-INSIGHTS)  
7. [Challenges](#challenges)
8. [Recommendation](#RECOMMENDATION)
13. [References](#references)  


## OVERVIEW 
This project deep dives into motor vehicle collisions (MVCs) in Toronto using historical data from 2014 to the present (2023).
* Built an interactive Tableau dashboard to visualize key insights on accident hotspots, contributing factors, and trends.
* The goal is to provide actionable insights to Toronto Police Service which includes policy makers, law enforcement, and city planners to enhance road safety.
* This project support the city of toronto Vision Zero Road safety Plan

## BACKGROUND & PROBLEM STATEMENT
Motor vehicle collisions are a major concern in urban areas, affecting public safety, infrastructure, and city planning. In Toronto, the city has committed to the **Vision Zero Road Safety Plan**, a comprehensive initiative aimed at reducing traffic-related fatalities and serious injuries on its streets. This project will contribute to the goals of Vision Zero by providing a data-driven, targeted approach for Toronto Police and city planners, enabling them to focus on the locations and factors where road safety improvements are most needed.

In Toronto:

* 35,000 - 40,000 MVCs occur annually, ranging from minor property damage to fatalities.
* High-risk locations, times, and factors contributing to accidents remain unclear without deep data analysis.

By analyzing historical trends and key collision factors, this project seeks to provide actionable insights to improve road safety policies, urban planning, and traffic management.

## AIM
The primary objective of this project is to identify trends and patterns in MVCs to support data-driven decision-making for safer roads.
Specifically, this project aims to:

Identify high-risk areas for targeted safety interventions.
Analyze how external factors (e.g., COVID-19, weather) impact collision rates.
Determine the time-of-day trends to guide law enforcement in deploying resources efficiently.
Assess the impact of driver behaviors (e.g., fail-to-remain incidents).
Help lawmakers and city officials take proactive measures to reduce road accidents.

## TECH STACK
  Category  | Technogies Used | Why?
  ------------- | ------------- | ------------
  Programming | Python 3.10.11| Python is a versatile and widely used programming language for data analysis, offering extensive libraries for handling large datasets. Due to its simple, readable syntax It makes data analysts jobs much more efficient 
  Data Processing | Pandas, Numpy  | Pandas provides powerful data manipulation and analysis capabilities, while NumPy enables efficient numerical computations
  Visualization | Tableau Public Desktop 2024.1.1 | Tableau has variety of features for making advanced interactive dashboard for simplifying data visualization for non-technical audience
  Environment | Jupyter Notebook | Jupyter Notebook is an ideal tool for analysts, as it provides an interactive environment for coding, visualization, and documentation in cell-by-cell format, making it easier to explore data and present insights effectively
  Data Validation | Excel | Excel offers great fratures for data validating data such as data validation rules, conditional formatting, and pivot tables to ensure accuracy and consistency in data.
## DATA 
  #### Data Collection
  * Source: Toronto Police Service (Public Data Repository) (Link: https://data.torontopolice.on.ca/datasets/bc4c72a793014a55a674984ef175a6f3_0/explore)
  * Data Type: Structured (CSV format)
  * Years Covered: 2014 – 2023
  * Number of Records: 635,000+ reported collisions
 #### Key Data Points 
  Feature | Description
  ------------- | -------------
  OCC_DATE | datetimestamp for each occurrence 
  OCC_MONTH | Month Collision Occurred  
  OCC_DOW | Day of Week Collision Occurred 
  OCC_YEAR | Year Collision Occurred 
  OCC_HOUR | Hour Collision Occurred
  DIVISION | Police Division where Collision Occurred 
  FATALITIES | Number of Person’s Killed associated with the Collision
  INJURY_COLLISIONS | Indicates whether a Collision had an associated Injury 
  FTR_COLLISIONS | Indicates whether a Collision was associated to Fail to Remain
  PD_COLLISIONS | Indicates Whether a Collision was associated to Property Damage 
  HOOD_158 | Identifier of Neighbourhood
  NEIGHBOURHOOD_158 | Name of the Neighbourhood where collision occurred
  LONG_WGS84 | Longitudinal Coordinates of rach collision
  LAT_WGS84 | Latitudinal Coordinates
  AUTOMOBILE | Indicates whether a Collision involved a person in an automobile 
  MOTORCYCLE | Indicates whether a Collision involved a person in a motorcycle 
  PASSENGER | Indicates whether a Collision involved a passenger in a motor vehicle 
  BICYCLE | Indicates whether a Collision involved a cyclist 
  PEDESTRIAN | Indicates whether a Collision involved a pedestrian 

  #### Cleaning and Processing

  * Handled missing values using imputation techniques.
  * Removed duplicates to maintain data integrity.
  * Standardized date/time formats for accurate time-series analysis.
  * Geocoded locations for spatial mapping.


## PROJECT OUTCOMES AND INSIGHTS
### 1) Total Collisions by each neighourboodhood 

   <p align="left">
  <img src="https://github.com/user-attachments/assets/7e8e4a8e-a72f-44e9-937f-339ffab5f85b" width="700" height="400" alt="Alt text">
   </p>
   
   *	West Humber-Clairville: This neighbourhood leads the list with an average of 1,497.84 collisions annually.
   *	Wexford/Maryvale: This area experiences an average of 1,403.45 collisions each year.
   *	York University Heights: With an average of 1,065.64 collisions per year, this neighbourhood ranks third.
   *	Bayfront-The Islands: This neighbourhood records an average of 1,009.62 collisions annually, indicating a high frequency of incidents.
   *	Milliken: Rounding out the top five, this neighbourhood witnesses an annual average of 960.04 collisions. 

   
### 2) Total 5 highest collisions neighourboodhood 
   <p align="left">
  <img src="https://github.com/user-attachments/assets/da0c9d7e-7309-45c7-bc7b-9ec88c989b3d" width="700" height="300" alt="Alt text">
   </p>
   
### 3) Total Yearly Occurance 
   <p align="left">
  <img src="https://github.com/user-attachments/assets/5ea8078a-585f-47d0-b647-259684eb7e4f" width="700" height="300" alt="Alt text">
   </p>

  * The graph shows an exponential growth trend in total yearly occurrences, peaking at 82.83k in 2019.
  * In 2020, coinciding with the start of the pandemic, there was a significant drop to half of the 2019 figure, resulting in 44.74k occurrences.
  * This reduced level remained consistent for two years.
  * In 2022, there was a resurgence with an increase of 25% in occurrences.
  * However, this was followed by a decrease of 15% in 2023.
  * These fluctuations highlight the impact of external factors on yearly occurrences.
   
### 4) Avg. Monthy Occurance Rate(%)

<p align="left">
  <img src="https://github.com/user-attachments/assets/bb5b84ba-e31b-4ed8-bfd9-95970eff8255" width="700" height="300" alt="Alt text">
   </p>
   
* January: The collision rate starts at 9.10%, which is one of the highest rates observed throughout the year. This could be due to winter weather conditions, which can make roads slippery and visibility poor.
* February: It slightly decreases to 8.86%, possibly due to improving weather conditions or effective winter driving campaigns.
* March & April: The rate continues to decrease to 8.03% in March and 7.48% in April, which is the lowest rate in the year. The arrival of spring could lead to better driving conditions, resulting in fewer collisions.

### 5) Avg. Hourly Occurance Rate(%)
   <p align="left">
  <img src="https://github.com/user-attachments/assets/b12f6119-a3af-44ce-b960-47b6f66e5977" width="700" height="300" alt="Alt text">
   </p>

   * The collision rate is highest during the afternoon hours (from 12 to 17), with the rate ranging from 6.52% to 8.33%. The peak rate of 8.33% is observed at 17, which could be due to increased traffic during the evening rush hour.

## CHALLENGES 

* Handling Missing Values: Selecting the appropriate imputation techniques to ensure data integrity without introducing bias.
* Data Availability & Quality: Sourcing clean, structured, and relevant datasets posed a challenge, requiring extensive preprocessing.
* Geospatial Mapping & Visualization: Accurately plotting collision data on maps and ensuring spatial relationships were correctly represented.
* Data Transformation & Processing: Performing necessary data transformations to enable accurate calculations and meaningful insights.

## RECOMMENDATION
  Based on our analysis, we propose the following recommendations:

* Focused Interventions: Allocate resources and interventions to the areas identified as having high collision rates. This could include increased traffic enforcement, improved road signage, or infrastructure changes.
* Public Awareness Campaigns: Initiate public awareness campaigns during the times identified as having a high occurrence of collisions. These campaigns could focus on safe driving practices and the importance of road safety.
*	Further Research: Conduct additional research into the types of vehicles involved in a high number of collisions. This could inform vehicle safety standards and regulations.
*	Data-Driven Planning: Continue to use data analysis in planning and decision-making processes related to road safety. This approach ensures that strategies are based on evidence and can effectively address the issues at hand.

## REFERENCES

* https://www.toronto.ca/services-payments/streets-parking-transportation/road-safety/vision-zero/vision-zero-plan-overview/
* https://data.torontopolice.on.ca/datasets/TorontoPS::traffic-collisions-open-data-asr-t-tbl-001/about
