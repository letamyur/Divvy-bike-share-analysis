# Divvy-bike-share-system-analysis
Hey! This is my first full-fledged analytical project created as part of the Google Data Analytics course.
## 1. Introduction.

This README file describes the work performed on the Divvy-tripdata dataset to evaluate users of the Divvy Bike Share System in the city of Chicago. Resources used include Python in conjunction with Jupyter Notebook and related packages Pandas and Numpy for data transformation and cleaning, as well as Tableau, which was applied for the analysis and visualization of the dataset.

**Project Goal:** Analyzing the difference in bicycle usage between annual members and casual riders to develop a marketing strategy aimed at attracting casual riders to annual membership.

**Key Questions:**
How does the behavior of annual members and casual riders differ?
What usage patterns are characteristic of each group?
What opportunities exist to attract casual riders to annual membership?

**Hypotheses:**
Given that the Divvy service is located in Chicago, a significant portion of casual riders are tourists.
Annual users are mostly students and employees who use bicycles on their way to work or study.

## 2. Description of Used Data.

The data for the project consists of historical data on individual bicycle trips made by users of the Divvy service, operating in Chicago, from the beginning of January to the end of December 2024.
The data has been made available by Motivate International Inc. under this [license.](https://divvybikes.com/data-license-agreement) And kindly provided by Google as part of the data analytics course.

Explore the data by downloading the last 12 months of [divvy-tripdata.](https://divvy-tripdata.s3.amazonaws.com/index.html)

### 2.1 Dataset Contents.

All data is divided into 12 separate csv format files, each containing records for a specific month. Here is a description of each column contained in each dataset.
* Ride ID (ride_id)
* Rideable Type (rideable_type)
* Time trip started (started_at)
* Time trip ended (ended_at)
* Start Station Name (start_station_name), Start Station ID (start_station_id)
* End Station Name (end_station_name), End Station ID (end_station_id)
* Latitude andlongitude of the start of the trip (start_lat, start_lng)
* Latitude andlongitude of the end of the trip (end_lat, end_lng)
* User type (member_casual)   

## 3. Data Cleaning and Transformation.

All stages of data cleaning, processing, and transformation, including Python code and comments, were documented in a [ipynb](divvy_trips.ipynb) file exported from Jupyter Notebook. This document contains a full description of the steps taken to prepare the data for analysis.
However, I will briefly describe my steps of the process of working on the dataset.
Since each individual dataset contained a large number of rows, and consequently a large file size, it was decided to use Python as one of the main tools for working on the project.

### 3.1 Data Cleaning and Preparation Process.

* To get an overall picture, we combine 12 separate files into one complete dataset.
* Checking for duplicates and empty values.
* Deleting unnecessary columns.
* Calculating trip duration.
* Extracting information about time, day, and month.
* The final process is grouping and calculation.
As a result of all cleaning processes, the dataset size was reduced from almost 6 million to 420 thousand rows.

## 4. Data Analysis Process.

For analysis and research, I chose the visualization tool Tableau, as it provides extensive opportunities for data exploration and the creation of interactive dashboards.
Gain some key isights by yourself using tis [dashboard](https://public.tableau.com/views/DivvyBikeShareSystem/DivvyBikeShareSystemDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
**Analysis Stages:**
* Building KPI indicators.
* Building individual charts.
* Creating filters.
* Constructing the dashboard.
* Analyzing and noting the obtained results.

### 4.1 Overview of Key Results.

* **General overview of the number of trips.**

![Image](https://github.com/user-attachments/assets/6e974b98-74e8-4791-9e8f-4c37fd259d03)

* **Both user groups share a common seasonality, preferring to use bicycles in the warmer months.**
![Image](https://github.com/user-attachments/assets/1143d17f-c927-40a5-8077-e178fd0c257d)

* **Regarding the distribution by bicycle type, both user types show a similar pattern in the use of classic and electric bicycles, but casual riders choose electric scooters significantly more often.**
![Image](https://github.com/user-attachments/assets/cba3b7d8-6a31-40f0-92e1-fdb5ae7ac6af)

### 4.2 Detailed Analysis of User Behavior.

Main patterns of each group and their differences from each other.

**Casual Riders:**

* **Weekends:** High activity on Saturday and Sunday, which may indicate the use of the service for leisure and recreation.
![Image](https://github.com/user-attachments/assets/d4c0daa6-a7e2-4a49-ba37-5c513fe772f2)

* **Usage Hours:** Casual riders use the service significantly more often in the afternoon and evening.
![Image](https://github.com/user-attachments/assets/ac5f6d55-294c-4ffd-a815-125c895514cc)

**Annual Members:**
* **Weekdays:** Stable use of the service throughout the weekdays with a decrease on weekends.
![Image](https://github.com/user-attachments/assets/d4c0daa6-a7e2-4a49-ba37-5c513fe772f2)

* **Usage Hours:** High rates during morning and evening peak hours, characteristic of commuting to work.
![Image](https://github.com/user-attachments/assets/ac5f6d55-294c-4ffd-a815-125c895514cc)

* **Trip Duration:** Annual users mostly use bicycles for trips lasting up to 20 minutes.
![Image](https://github.com/user-attachments/assets/47b262db-3083-4ee0-8df3-529abfa0dc0a)

**Main differences between groups.**
* **Bicycle Types:** Casual riders have a greater preference for using electric scooters compared to annual members.
![Image](https://github.com/user-attachments/assets/cba3b7d8-6a31-40f0-92e1-fdb5ae7ac6af)
* **Trip Duration:** The number of trips lasting 40-60 and over 60 minutes is higher among casual riders than annual members, which supports the hypothesis of a potentially large number of tourists among them.
![Image](https://github.com/user-attachments/assets/47b262db-3083-4ee0-8df3-529abfa0dc0a)

## 5. Key Insights.

Analysis of the Divvy bike share service trip data revealed significant differences in behavior between annual members and casual riders, which confirms the initial hypotheses.

The data confirms the hypothesis that a significant portion of casual riders are tourists, as they exhibit usage patterns characteristic of tourist activity: significantly higher activity on weekends, when the sun has not yet set below the horizon, and behavior typical of tourists, when they use bicycles to explore the city's attractions, as evidenced by the higher number of trips over 40 minutes compared to annual members. Their activity during the week is less intense, and usage hours are shifted to later times of the day.
The analysis also confirms the hypothesis that annual users are mostly students and employees who use bicycles for daily commutes to work or study (the so-called "nine to five" schedule). This is confirmed by their stable use of the service throughout the week with clear morning and evening peaks, which corresponds to the typical commuting schedule.
The conclusions clearly demonstrate the different needs and usage patterns of the service by these two user groups.

## 6. Recommendations for Marketing Strategy.

### Recommendation 1: Implementation of Short-Term Memberships.
Consider introducing flexible short-term memberships, such as weekly, monthly, or seasonal (e.g., summer), specifically designed to attract tourists and local casual riders who are not interested in an annual membership. This will allow reaching a wider audience that actively uses the service during certain periods and potentially increase company revenue.

### Recommendation 2: Launch of Targeted Marketing Campaigns on Weekends.
Since casual riders show significantly higher activity on weekends, it is recommended to focus marketing efforts specifically on this period. Campaigns can emphasize the benefits of annual membership for leisure activities, city exploration, and sightseeing, as well as potential cost savings with regular weekend use of the service.

### Recommendation 3: Establishing Partnerships with the Tourism Infrastructure.
To effectively attract tourists, who constitute a significant portion of casual riders, it is proposed to establish partnerships with hotels, tourist agencies, information centers, and other organizations operating in the tourism sector. This may include placing promotional materials, offering special service packages, or implementing partner loyalty programs.
