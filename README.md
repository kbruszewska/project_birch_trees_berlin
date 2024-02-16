# project_birch_trees_berlin
## Project title
### Why do birch trees die in Berlin?

## Motivation
The aim of the project is to explore the correlation between the increased felling of birch trees in the city of Berlin and potential underlying factors. A primary consideration is the impact of climate change. Therefore, the project closely examines various weather parameters such as temperature and precipitation to address this inquiry. Case study chosen for the project is one of the districts in Berlin called Friedrichshain-Kreuzberg. 
The author, who possesses a robust background in natural sciences and landscape design, selected this research topic based on personal observations made over the last three to four years within Berlin, where she resides.

## Dataset Information 
To conduct the project the following data was collected and analysed:
* Tree felling lists for the case study district Friedrichshain-Kreuzberg in Berlin for following years: 2017 till 2023:
https://www.berlin.de/ba-friedrichshain-kreuzberg/politik-und-verwaltung/aemter/strassen-und-gruenflaechenamt/gruenflaechen/baeume/ 
* Weather/ climate parameters (recent from 07.08.2022 till 07.02.2024) from Deutscher Wetterdienst: 
Recent daily station observations (temperature, pressure, precipitation, sunshine duration, etc.)
https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/daily/kl/recent/
* Weather/ climate parameters (historical until 31.12.2022) from Deutscher Wetterdienst:
Historical daily station observations (temperature, pressure, precipitation, sunshine duration, etc.)
https://opendata.dwd.de/climate_environment/CDC/observations_germany/climate/daily/kl/historical/
* The weather was taken from the station with the station_id 433. 

## Project description and how to use 
### Goals, methodology and conclusions
The main goal of the project was to find out the possible reasons for the more intensive dying of birch trees in the city of Berlin. Birch trees are a typical species for this part of Europe and are also considered pioneer species capable of thriving even on slopes. However, the observed phenomenon contrasts with the natural characteristics of the tree.


The case study district is located in a central area of Berlin and is characterized by a typical urban climate. The available data helped to gain an overview of the felled trees and the reasons for that within the time frame of the last 7 years (2017-2023). Birch trees constitute a significant portion of the dataset, comprising over 5%.


Based on the analyzed meteorological data, significant climate changes have been observed, such as much less yearly precipitation over the last 10 years (8 out of 10 years with less than the average precipitation). Concurrently, the number of dry days has increased, reaching very high levels in some years. Additionally, there are more hot days with temperatures exceeding 30°C, and a significant increase in the average yearly temperature in recent years.


The conducted analysis confirms a close correlation between unusual weather phenomena in recent years, such as in 2018, and their influence on tree health. Based on the conducted analysis the close correlation between the unusual weather phenomena last years, such as year 2018, can be confirmed. 


One of the final conclusions of the project is that due to the shifting city climate in Berlin, birch trees may no longer be suitable for planting here. This could be an important finding for stakeholders and city planners, who should consider alternative tree species for planting in the city of Berlin.


### Steps to conclude the project:
1. Creating a project borad on Trello
- https://trello.com/b/X9i41wMw
2. Notebook file trees:
- Data files for felling trees were imported and cleaned (for example renaming columns, adding columns for year, subdistrict, removing null values). As output 14 tables were created.
3. Notebook file trees_all:
- In the next step, all tables were concatenated into one table containing data on all felled trees. During this process, certain columns deemed unnecessary for further analysis were dropped. The resulting table comprised 3506 individual trees.
A total of 171 different reasons for felling trees were identified in the dataset. To efficiently identify and combine these reasons, the Python library RegEX was utilized. Subsequently, the reasons were grouped into 8 main categories and translated into English. Interestingly, reasons such as diseases were not cited as causes for felling birch trees.
Finally, the clean data was exported both as a CSV file and into a MySQL database. At this stage, the table still consisted of 3506 individual trees.
4. Notebook file climat:
- Datasets containing historical and recent climate parameters were imported, cleaned, and concatenated. During this process, certain features were removed as they were deemed unnecessary for further analysis. Additionally, new features such as year, month, and day were created by extracting relevant information from existing features.
Once the data was prepared, it was exported to both a CSV file and a MySQL database for further analysis and integration with other datasets.
5. Working in MySQL
- Datasets with climate and trees were read and analysed in MySQL.
6. Notebook file project_trees:
- The data frame containing data for trees and climate between the years 1993-2023 was imported from MySQL to Python using a query. Subsequently, the data was analysed and explored.
Next, a hypothesis was formulated and evaluated, positing that the average yearly temperature within the last 10 years (2014-2023) is higher than the average yearly temperature within the previous years (1948-2013). To test this hypothesis, the dataset spanning the entire available time period (1948-2023) was imported from MySQL.
Using a one-sided test, the null hypothesis could not be rejected, indicating that the average temperature in the previous years was lower than in the last 10 years.
7. The further analysis and visualisations were conducted in Tableau:
- Link to Tableau https://public.tableau.com/views/project_trees_final/Temp3?:language=de-DE&:sid=&:display_count=n&:origin=viz_share_link
8. Presentation it attached in the documentation. 

## Tech/framework used
Python: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn(Sklearn), SciPy, RegEX, PyMySQL.
Jupyter Notebook
Anaconda
MySQL
Tableau
GitHub
GitBash
Trello

## Features
Combining the data analytics techniques to the city planning. 

## Installation
Used version Python 3.11.5


You would be needing multiple libraries such as Math, Numpy, Pandas and Seabon for basic operations and many pre-processing and ML Model libraries.
- pip install [Library_Name] 

  
