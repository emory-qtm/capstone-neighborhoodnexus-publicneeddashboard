# Emory QTM Capstone: Neighborhood Nexus - Public Need Dashboard
Covid-19 is having a considerable impact on the wellbeing of Americans and changed the way many nonprofit organizations operate and deliver services. Similarly, rapid changes in the needs of Americans led to shifting priorities and demand in the nonprofit sector. There is an immediate demand forup-to-date information on public sentiment and areas of need to allow nonprofits to rapidly respond to changes and leverage their resources in a more effective way.


## Table of contents
- [Motivation](#motivation)
- [Project Partners](#project-partners)
- [Intended User](#intended-user)
- [Intended Use](#intended-use)
- [Installation](#installation)
- [Setup](#setup)
- 
      - [Google API Sheet](#google-api-sheet)
      - [Dashboard](#dashboard)
- [Dashboard](#dashboard)
- 
      - [Intended Use](#intended-use)
- [Acknowledgements](#acknowledgements)


# Motivation


# Project Partners


# Intended User

If you are interested in learning about what people in the U.S. are demanding for or are passionate about helping non-technical audiences keep track of up-to-date information on public sentiments, then this project is right for you! This repo is designed for Python users who want to build an interactive real-time data reporting dashboard on the most popular social issues in the Atlanta metropolitan area, such as housing, healthcare, and employment. 

# Intended Use

This Github repository allows users to easily extract qualitative data on socioeconomic topics and build a real-time interactive dashboard upon it. A typical user of this Github repository should be interested in using data from non-profit organizations, Census Bureau, and Google queries, as these three data sources represent an integral image of diverse American needs. Our dashboard acts as a one-stop platform for users to access these three data sources, to visualize the popular social issues today, and to understand the rising demands in the nonprofit sector.  

## Data sources:

### 1. United Way AIRS data:
Because our stakeholder, Neighborhood Nexus, is partnering with United Way Worldwide, a non-profit organization that has over 1,800 affiliates globally, our team obtained monthly data from AIRS (Alliance of Information and Referral Systems) that informs us on the Problem Needs and Referred and Unmet Services. This data is used to reflect the real-time requests from people in Georgia on our dashboard. 

### 2. Google Trends data (https://trends.google.com/trends/?geo=US):
Because Google Trends data is comprehensive, publicly available, updated frequently, our team mainly used this data source to visualize the historical and geographical trends of 17 most popular topics, as well as comparing the topic popularity in Georgia with the average topic popularity in the U.S. Users can use our “Data Extraction: Google Trends” file to understand our datasets better.

### 3. Census Bureau data (https://www.airs.org/i4a/pages/index.cfm?pageid=1): 
The Annual Resident Population Estimates by Age, Sex, Race, and Hispanic Origin; for the United States, States, and Puerto Rico: April 1, 2010 to July 1, 2019, from Census Bureaus, was used to reflect recent demographic trends on race, population, and geographical locations in the Atlanta Metropolitan area. Users can rely on this data source to visualize popular social issues within different ethnic groups in different counties. 

## Dashboard:
Our real-time interactive dashboard (https://datastudio.google.com/reporting/6ac7cce1-b42c-412f-ab3e-03f1a1995886) allows both technical and non-technical users to easily navigate and explore rising public sentiments on a variety of social topics today. More details can be found in the “Dashboard” section. 

With the use of our data sources and dashboard, users will be informed on the real-time, historical, geographic, and demographic trends of 17 important topics in the nonprofit sector


# Installation 

To begin, install and ensure that you have the latest version of each
>     - pip install pytrends
>     - pip install gspread
>     - pip install gtab

# Setup


## Google API Sheet

## Dashboard 

# Dashboard

## Overview

This dashboard strives to help nonprofit organizations in Georgia resolve or alleviate the problem of responding to rapid changes in public sentiments that need quick attention. It aims to provide both real-time and historical insights of topics that are relevant to nonprofit services. In this way, these organizations would be able to monitor real-time changes in the needs of people in Georgia and visualize past trends in these needs. To achieve this, we incorporated different types of data visualizations to present the data in a more user-friendly way while displaying the most important information. We also embedded filter controls so that users of this dashboard may navigate more easily and change the outlook according to their interests if needed.

## Intended Use

In general, a user may launch the dashboard when he/she wants to:
- Look for trending topics
- Look for topic popularities
- Compare popularities in Georgia and popularities in the US of different topics
- Explore historical trends of popularities of selected topics
- Explore how popularities of one topic differ throughout different regions in Georgia
- Explore if there exists a relationship between the demographic data and the popularity data throughout different regions in Georgia

Note: For any of the above use cases, the user should set a certain date range of interest since all charts depend on the date range.

### Real-time Insights

The real-time section consists of:

(a) A table that represents the counts of inquiries for different AIRS problem needs

(b) A bar graph that compares average popularities in Georgia and average popularities in the United States of different topics

(c) A bubble map that presents difference in popularities of a certain topic in Georgia areas

**Filter Control and Data Source:** (a), (b), and (c) are controlled by the same date range filter. (a) does not use a topic filter and is controlled by AIRS data source, while (b) and (c) use the same topic filter and are both controlled by Google Search Trends data. 

**Use Case:** The user may look at (a) when he/she wants to look for the most trending needs of people in Georgia. (b) and (c) are ideal for comparisons of popularities from different geographical levels. Specifically, (b) compares popularities in Georgia to the national level, while (c) compares popularities in different regions of Georgia.

### Historical Trends

The historical section consists of a line graph that presents trends of different topics.

**Filter Control and Data Source:** It is controlled by a date range filter and a topic filter. The data source comes from Google Search Trends data. 

**Use Case:** This section is useful when the user wants to explore how popularities of different topics change over time, indicated by peaks and inclinations in lines.

### Demographic Trends

The demographic section consists of a bubble map that presents supplemental, demographic information in different areas of Georgia.

**Filter Control and Data Source:** It is controlled by an indicator filter and a date range filter. The data source is Georgia Census Data.

**Use Case:** It is recommended that the user compares the bubble map in the section with the one in the real-time section to see if there exists any relationship between topic popularities and demographic indicators in different regions of Georgia. For example, if a user finds out that Atlanta has the highest popularity for housing and the highest proportion of minorities over other regions, it may indicate that there is a positive relationship between the two. However, it is encouraged that users should always evaluate how explanatory their finding is before making a conclusion.

## Data Sources
* Google Search Trends 
* United Way 211 - Atlanta 
* Census - (include specific file name)

# Acknowledgements
