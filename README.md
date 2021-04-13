# Emory QTM Capstone: Neighborhood Nexus - Public Need Dashboard

## Table of contents
- [Motivation](#motivation)
- [Project Partners](#project-partners)
- [Intended Use of Project](#intended-use-of-project)
  * [Use Case](#use-case)
  * [Use of Data Sources](#use-of-data-sources)
  * [Use of Dashboard](#use-of-dashboard)

- [Installation](#installation)
- [Setup](#setup)
  * [Google API Sheet](#google-api-sheet)
  * [Dashboard](#dashboard)
- [Dashboard](#dashboard)
  * [Overview](#overview)
  * [Intended Use of Dashboard](#intended-use-of-dashboard)
  * [Data Sources](#data-sources)
- [Acknowledgements](#acknowledgements)


# Motivation

The main motivation behind this project is to help non-profit organizations in Georgia quickly respond to public sentiments. Many people need assistance from organizations that can help them improve their mental state and relieve stress. The Covid-19 pandemic has cut into nonprofits’ resources while increasing and changing the needs of Americans. This has led to  shifting priorities and demand in the nonprofit sector. There is an immediate demand for up-to-date information on public sentiment and areas of need to allow nonprofits to rapidly respond to changes and leverage their resources in a more effective way. So far, there has been a gap between what nonprofits do and what people really need. That is, without access to up-to-date information on public sentiment and areas of need, it is hard for nonprofits to deliver optimal services based on people’s true needs.

Therefore, as a group of students who are passionate about the applications of data science in nonprofits, we aim to create a real-time interactive dashboard. This will serve as a tool for non-profits and human service agencies to understand and respond to areas of need in order to improve the quality of life for the residents of Georgia. With this dashboard, we will be able to solve the problem by filling the gap of information as well as meeting the demands of most recent sentiment data. The dashboard is open to the public and uses open-sourced and publicly available data to understand public sentiment. Thus, it can create collaboration between organizations by collecting valuable insights from leaders and distributing those insights back to them. The dashboard will provide actionable data that conveys indicators and trends which can serve as a predictive measure for non-profits along with helping in a wide variety of ways such as designing programs, making investments and allocating resources. 


# Project Partners

# Intended Use of Project

A typical user of this Github repository should be interested in 
- learning about what people in Georgia are demanding for 
- helping non-technical audiences keep track of up-to-date information on public sentiments
- analyzing data from non-profit organizations, Census Bureau, and Google search queries, as these three data sources represent an integral image of diverse American needs. 

This repo is designed for Python and Google Data Studio users who want to build an interactive real-time data reporting dashboard on the most popular social issues in the Atlanta metropolitan area, such as housing, healthcare, and employment. 

## Use Case

This Github repository allows users to:
- easily extract qualitative data on social problems
- build a real-time interactive dashboard upon extracted data. 

Our dashboard acts as a one-stop platform for users to: 
- access three data sources, including United Way AIRS data, Google Trends data, and Census Bureau data
- understand the rising demands for nonprofit services
- visualize historically and currently trending topics in the nonprofit sector


## Use of Data sources

#### 1. United Way AIRS data:
Because our stakeholder, [Neighborhood Nexus](https://neighborhoodnexus.org/), is partnering with United Way Worldwide, a non-profit organization that has over 1,800 affiliates globally, our team obtained monthly data from AIRS ([Alliance of Information and Referral Systems](https://www.airs.org/i4a/pages/index.cfm?pageid=1)) that informs us on the Problem Needs, Referred services, and Unmet Services. 
This data is used to reflect the monthly ranking of what people in Georgia are requesting for on our dashboard. Because of privacy concerns, the AIRS dataset is not publicly avaiable.

#### 2. [Google Trends data](https://trends.google.com/trends/?geo=US):
Because Google Trends data is comprehensive, publicly available, updated frequently, this data source is used to visualize the historical and geographical trends of 17 most popular topics, as well as comparing the topic popularity in Georgia with the average topic popularity in the U.S. Users can use our *Data extraction_Google trends* file to understand our datasets better.

#### 3. [Census Bureau data](https://api.census.gov/data/2019/pep/charage.html): 
*The Annual Resident Population Estimates by Age, Sex, Race, and Hispanic Origin*; for the United States, States, and Puerto Rico: April 1, 2010 to July 1, 2019, from Census Bureaus, is used to reflect recent demographic trends on race, population, and geographical locations in the Atlanta Metropolitan area. Users can rely on this data source to visualize popular social issues within different ethnic groups in different counties. 

## Use of Dashboard
Our [real-time interactive dashboard](https://datastudio.google.com/reporting/6ac7cce1-b42c-412f-ab3e-03f1a1995886) allows both technical and non-technical users to easily navigate and explore rising public sentiments on a variety of social topics today. More details can be found in the *Dashboard* section. 

With the use of our data sources and dashboard, users will be informed on the real-time, historical, geographic, and demographic trends of 17 important topics in the nonprofit sector


# Installation 

To begin, install and ensure that you have the latest version of each
>     - pip install pytrends
>     - pip install gspread
>     - pip install gtab
>     - pip install oauth2client

# Setup

## Google API Sheet

1.    Go to [Google Developers Console](https://console.cloud.google.com/) and sign in to your Google account
2.    Create a new project
![img1](/images/img1.png)
3.    Search for and Click *ENABLE* the Google Drive and the Google Sheet APIs
![img2](/images/img2.png)
![img3](/images/img3.png)
4.    Create credentials for *Web Server* to access Application Data
![img4](/images/img4.png)
5.    Download **your own the JSON file** (e.g. projectname-id.json)
6.    Copy the JSON file to your code directory
      - Its file path is used for data extraction
7.    Initialize the Google Sheet for each dataset
      - Copy the *client_email* in JSON file and add it to *the Google Sheet Editor* for each dataset

## Dashboard 

1.    Go to [Google Data Studio](https://datastudio.google.com/)
2.    Create a new report
![img5](/images/img5.png)
3.    Connect your data sources by using Google Sheets Connectors
![img6](/images/img6.png)
4.    Add charts
![img7](/images/img7.png)
5.    Customize the formatting and add a title and captions

# Dashboard

## Overview

This [real-time interactive dashboard](https://datastudio.google.com/reporting/6ac7cce1-b42c-412f-ab3e-03f1a1995886) strives to help nonprofit organizations in Georgia resolve or alleviate the problem of responding to rapid changes in public sentiments that need quick attention. It aims to provide both real-time and historical insights of topics that are relevant to nonprofit services. In this way, these organizations would be able to monitor real-time changes in the needs of people in Georgia and visualize past trends in these needs. To achieve this, we incorporated different types of data visualizations to present the data in a more user-friendly way while displaying the most important information. We also embedded filter controls so that users of this dashboard may navigate more easily and change the outlook according to their interests if needed.

## Intended Use of Dashboard

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
* [Google Search Trends data](https://trends.google.com/trends/?geo=US) 
* United Way AIRS data - Georgia, U.S. 
* [Bureau Census data](https://api.census.gov/data/2019/pep/charage.html)

# Acknowledgements

- [Neighborhood Nexus](https://neighborhoodnexus.org/)
- [Emory QTM Department](http://quantitative.emory.edu/)
- [United Way Atlanta](https://www.unitedwayatlanta.org/)
