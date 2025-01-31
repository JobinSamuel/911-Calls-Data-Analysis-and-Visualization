**911 Calls Analysis Capstone Project
Overview**
This project provides an in-depth analysis of a dataset containing information about 911 emergency calls. The dataset was sourced from Kaggle and includes a wide range of features such as call description, location, and time details. The analysis aims to uncover insights into the data, including identifying trends and patterns in emergency call types, times, and locations.

The dataset contains the following features:

lat: Latitude of the call.
lng: Longitude of the call.
desc: Description of the emergency call.
zip: Zipcode of the location.
title: Title specifying the type of emergency.
timeStamp: Time the call was made (YYYY-MM-DD HH:MM
).
twp: Township where the call originated.
addr: Address of the emergency.
e: Dummy variable for future use.

**Key Objectives
**Explore the distribution of emergency calls across locations and time.
Identify the most frequent types of emergencies.
Visualize trends using various plots, such as count plots, time series plots, and heatmaps.

**Dataset Information
**The dataset contains 99,492 entries and 9 columns. Each entry corresponds to a 911 emergency call made in a particular township. Below are the data types for each column after loading the dataset:


**Analysis and Insights
****1. Top 5 Zipcodes for 911 Calls
**By using the .value_counts() method, we can identify the top 5 zip codes with the most 911 calls:

Zip code 19401 has the highest number of calls with 6,979.
Other frequent zip codes include 19464, 19403, 19446, and 19406.

**2. Top 5 Townships (Twp) for 911 Calls
**Similarly, the most common townships for 911 calls were identified:

LOWER MERION is the most frequent township with 8,443 calls, followed by ABINGTON, NORRISTOWN, UPPER MERION, and CHELTENHAM.

**3. Analysis of Emergency Call Types
**The title column contains information about the type of emergency. By applying a lambda function, we can extract the type of emergency (e.g., EMS, Fire, Traffic):
EMS: 48,877 calls.
Traffic: 35,695 calls.
Fire: 14,920 calls.

**4. Temporal Analysis
**Using the timeStamp column, we created additional time-based features, such as Hour, Month, and Day of Week. These were used to generate insights about the times and days when emergencies are most frequent.

We then generated various plots, including:

Countplot by Reason: Showed the distribution of call types across different times of the day and days of the week.
Time Series Plot by Reason: Allowed us to explore trends in the data over time for different emergency types.

**5. Heatmaps and Clustermaps
**Heatmaps and clustermaps were used to visualize the distribution of calls based on Hour, Day of Week, and Month. This highlighted temporal patterns in emergency call volumes.

**Visualizations
****1. Countplot of Emergency Calls by Reason
**
**2. Time Series of 911 Calls by Month
**A simple line plot to display the total number of 911 calls over each month:

**3. Heatmap of Calls by Hour and Day of the Week
**The heatmap shows how emergency call frequencies change over the day and across the week:

**4. Clustermap of Calls by Hour and Day of the Week
**Clustermaps allow us to identify patterns by clustering similar behaviors together:

**Project Workflow
**
Data Loading: The data is loaded using Pandas and initially inspected using .info() and .head().
Exploratory Data Analysis: The data is explored using basic functions such as .value_counts(), and new columns (e.g., Reason, Hour, Month, Day of Week) are created to assist with the analysis.
Visualizations: Seaborn and Matplotlib are utilized to create visual representations of the data, including count plots, time series, and heatmaps.
Conclusions: The analysis provides valuable insights into when and why 911 calls are made, which can help emergency services improve their response strategies.

**Files in the Repository
**911_Analysis.ipynb: Jupyter notebook containing all analysis and visualizations.
911.csv: Dataset used for the analysis.
README.md: Project overview and explanation.

**Conclusion
**This project demonstrates how we can analyze real-world 911 call data to uncover meaningful patterns and trends. These insights can be invaluable for emergency response teams to allocate resources more effectively based on the time and type of calls.
