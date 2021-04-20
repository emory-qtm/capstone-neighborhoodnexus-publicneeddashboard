# Emory QTM Capstone: Neighborhood Nexus - Public Need Dashboard                                                                      
![Logo](/images/Logo.png)

Our project aims to develop a platform that displays people’s current sentiment and needs in Georgia. Our dashboard displays current social service requests as well as trending search topics, allowing organizations to gain a better understanding of Georgia communities.

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

Therefore, as a group of students who are passionate about the applications of data science in nonprofits, we aim to create a real-time interactive dashboard. This will serve as a tool for non-profits and human service agencies to understand and respond to areas of need in order to improve the quality of life for the residents of Georgia. With this dashboard, we will be able to solve the problem by filling the gap of information as well as meeting the demands of most recent sentiment data. The dashboard is open to the public and uses open-source and publicly available data to understand public sentiment. Thus, it can create collaboration between organizations by collecting valuable insights from leaders and distributing those insights back to them. The dashboard will provide actionable data that conveys indicators and trends which can serve as a predictive measure for non-profits along with helping in a wide variety of ways such as designing programs, making investments and allocating resources. 


# Project Partners

We collaborated on this project with Neighborhood Nexus(https://neighborhoodnexus.org/), a nonprofit committed to providing organizations with the tools they need to ask the right questions, use meaningful data, and make informed decisions. Neighborhood Nexus helps organizations better understand the communities and situations they collaborate with by committing to provide high-quality, easily accessible data.

For this project Neighborhood Nexus laid out the guidelines, supplied United Way AIRS data, and provided feedback for our dashboard to convey current public sentiment to better inform nonprofit leaders. 


# Intended Use of Project

A typical user of this Github repository should be interested in: 
- learning more about what people in Georgia are searching for and determining areas of need
- keeping track of top trending topics and up-to-date information on public sentiments
- analyzing data from non-profit organizations, Census Bureau, and Google search queries, as they represent a holistic view of people's needs. 

This repo is designed for Python and Google Data Studio users who want to build an interactive real-time data reporting dashboard on the most popular social issues in the Atlanta metropolitan area, such as housing, healthcare, and employment. It can also help non-profits and human service agencies invest resources wisely and design effective programs for people and communities.  

## Use Case

This Github repository allows users to:
- easily extract qualitative data on social problems
- access extracted data from Google Trends and Census Bureau 
- build a real-time interactive dashboard using extracted data 

Our dashboard acts as a one-stop platform for users to: 
- access three data sources: United Way AIRS data, Google Trends data, and Census Bureau data
- understand the rising demands for nonprofit services
- visualize historically and currently trending topics in the nonprofit sector


## Use of Data sources

#### 1. United Way AIRS data:
Our stakeholder, [Neighborhood Nexus](https://neighborhoodnexus.org/), is partnering with United Way Worldwide, a non-profit organization that has over 1,800 affiliates globally. Thus, our team obtained monthly data from AIRS ([Alliance of Information and Referral Systems](https://www.airs.org/i4a/pages/index.cfm?pageid=1)) that informs us on the Problem Needs, Referred Services, and Unmet Services. 
This data is used to reflect the monthly ranking of what people in Georgia are requesting/searching for on our dashboard. Due to privacy concerns, the AIRS dataset is not publicly avaiable.

#### 2. [Google Trends data](https://trends.google.com/trends/?geo=US):
Google Trends data is comprehensive, open-source, publicly available, and updated frequently. Hence, this data source is used to visualize the historical, real-time and geographical trends of 17 most popular topics, as well as comparing the topic popularity in Georgia with the average topic popularity in the U.S. Users can use our *Data extraction_Google trends* file to understand our datasets better.

#### 3. [Census Bureau data](https://api.census.gov/data/2019/pep/charage.html): 
The Census Bureau dataset- *The Annual Resident Population Estimates by Age, Sex, Race, and Hispanic Origin; for the United States, States, and Puerto Rico: April 1, 2010 to July 1, 2019*, is used to reflect demographic trends on race, population, and geographical locations in the Atlanta Metropolitan area. Users can use this to understand the dashboard holistically by taking into account social and demographic factors like race and population in different counties in Georgia which may affect trending topics. 

## Use of Dashboard
Our [interactive dashboard](https://datastudio.google.com/reporting/6ac7cce1-b42c-412f-ab3e-03f1a1995886) allows both technical and non-technical users to easily navigate and explore rising public sentiments on a variety of social topics in real time. More details can be found in the *Dashboard* section. 

Through the use of our data sources and dashboard, users will be informed on the real-time, historical, geographic, and demographic trends of 17 important topics within the nonprofit sector.


# Installation 

To begin, install and ensure that you have the latest version of *pytrends, gtab, gspread, oauth2client*. This project requires Python >= 3.7.

Unix/macOS
>     - python3 -m pip install pytrends
>     - python3 -m pip install gspread
>     - python3 -m pip install gtab
>     - python3 -m pip install oauth2client

Windows
>     - py -m pip install pytrends
>     - py -m pip install gspread
>     - py -m pip install gtab
>     - py -m pip install oauth2client

Jupyter Notebook
>     - !pip install pytrends
>     - !pip install gspread
>     - !pip install gtab
>     - !pip install oauth2client

# Setup

## Google API Sheet

1.    Go to [Google Developers Console](https://console.cloud.google.com/) and sign in to your Google account
2.    Create a new project
![img1](/images/img1.png)
3.    Search for and click *ENABLE* the Google Drive and the Google Sheet APIs
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
4.    Add charts and data visualizations
![img7](/images/img7.png)
5.    Customize the formatting and add title and captions

# Dashboard

## Overview

This [real-time interactive dashboard](https://datastudio.google.com/reporting/6ac7cce1-b42c-412f-ab3e-03f1a1995886) strives to help non-profit organizations in Georgia resolve or alleviate the problem of responding to rapid changes in public sentiments that need quick attention. It aims to provide both real-time and historical insights of topics that are relevant to non-profit services. In this way, these organizations would be able to monitor real-time changes and visualize past trends in the needs of the residents of Georgia. To achieve this, we incorporated different types of data visualizations to present the data in a more user-friendly way while displaying relevant information. We also embedded filter controls so that users of this dashboard may navigate easily through topics and set time frames based on their interest.

## Intended Use of Dashboard

In general, a user may launch the dashboard when he/she wants to:
- Search for trending topics in Georgia
- Search for topic popularities within Georgia
- Compare topic popularities of Georgia vs. the rest of US
- Explore historical trends within selected topics
- Explore the difference in topic popularities between different counties in Georgia
- Check for a relationship between demographic data and topic popularities throughout different counties in Georgia

Note: For any of the above use cases, the user should set a specified date range based on interest since all charts depend on the time frame.

### Real-time Insights

The real-time section consists of:

(a) A table that represents the counts of inquiries for different AIRS problem needs

(b) A bar graph that compares average popularities in Georgia vs. the United States of different topics

(c) A bubble map that represents difference in topic popularities within parts of Georgia

**Filter Control and Data Source:** (a), (b), and (c) are controlled by the same date range filter. (a) does not use a topic filter and is controlled by AIRS data source, while (b) and (c) use the same topic filter and are both controlled by Google Search Trends data. 

**Use Case:** The user may look at (a) when he/she wants to look for the most trending needs of people in Georgia. (b) and (c) are ideal for comparisons of popularities from different geographical levels. Specifically, (b) compares popularities in Georgia to the national level, while (c) compares popularities within different regions of Georgia.

### Historical Trends

The historical section consists of a line graph that represents trends of different topics over time (January 2019 - March 2021).

**Filter Control and Data Source:** It is controlled by a date range filter and a topic filter. The data source comes from Google Search Trends data. 

**Use Case:** This section is useful when the user wants to explore how popularities of different topics change over time, indicated by fluctuations (peaks and troughs) in lines.

### Demographic Trends

The demographic section consists of a bubble map that shows supplemental demographic information for different counties of Georgia.

**Filter Control and Data Source:** It is controlled by an indicator filter and a date range filter. The data source is Census Bureau Data.

**Use Case:** It is recommended that the user compares the bubble map in the demographic section with that of the real-time section to see if there exists any relationship between topic popularities and demographic indicators in different regions of Georgia. For example, if a user finds out that Atlanta has the highest popularity for housing and the highest proportion of minorities over other regions, it may indicate that there is a positive relationship between the two. However, it is encouraged that users should always investigate further and check for other factors before reaching any conclusion.

## Data Sources
* [Google Search Trends data](https://trends.google.com/trends/?geo=US) 
* [Census Bureau data](https://api.census.gov/data/2019/pep/charage.html)
* United Way AIRS data - Georgia, U.S. 

# Acknowledgements

- [Neighborhood Nexus](https://neighborhoodnexus.org/)
- [Emory QTM Department](http://quantitative.emory.edu/)
- [United Way Atlanta](https://www.unitedwayatlanta.org/)
- [Alliance of Information and Referral Systems](https://www.airs.org/i4a/pages/index.cfm?pageid=1)
