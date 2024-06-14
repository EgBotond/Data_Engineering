# Data_Engineering

## Project Description:
This project serves as the culmination of my data engineering training and aims to showcase my current skills and knowledge in this field. It will also serve as a foundation for a continuously expanding portfolio. Due to my future goals and responsibilities, the project places a strong emphasis on tools for data collection from online platforms, such as web scraping and data collection via APIs. The latter forms the data sources for an ETL pipeline built within an extensive AWS cloud environment, whose results are then used for local tasks, in this case, creating visualizations.

### Web Scraping Elements:
In general, these are based on the BeautifulSoup library running in Python 3.11 and 3.12, along with a development environment consisting of other supporting packages. In the near future, I plan to incorporate elements based on the Selenium package into my currently ongoing projects. My goal with these is not only reliable and accurate data collection but also to create a more accessible input interface, facilitating future Streamlit integration.

#### Alternative_ways_to_scrape_com_areas.ipynb: 
A method based on the ssl package and utilizing Wikipedia's comparatively straightforward HTML layout for gathering data table material from pages. Later on, the Taxi project directly included this. It's interesting to see that BeautifulSoup was not even needed for scraping in this method.

#### Foursquare_scraper_by_city.ipynb:
This application gathers information from a well-known, internationally active website. The user-generated list of the top 30 local businesses and attractions on Foursquare is based on the input of the city name.

#### Guardian_scraper_project.ipynb: 
This program uses a technique based on the BeautifulSoup library to gather articles published on a given date from any news feed of The Guardian, an international news website. The initial input values are the URL of the news feed and the desired date, provided through a pre-programmed graphical interface. If the news feed stores articles in monthly containers, the program recognizes this and scrapes all articles from the month of the specified date. The result of the run includes the titles, dedicated URLs, and publication dates of the articles, compiled into an accessible database. The second part of the program generates a summary of a selected article using NLP algorithms and, for quicker overview, also creates a word cloud based on the summary.

### Taxi Project in AWS
#### AWS ETL - 07_whole_AWS_ETL_10th_week_HW.ipynb:
This part of the project is a standalone work covering various aspects of the AWS cloud environment. It extracts official data sources from the city of Chicago and weather data from open-meteo.com into specified folders in an AWS S3 Bucket data lake, which I have automated using a daily refresh trigger. The daily refresh of the data sources triggers the transform and load parts of the program, performing data wrangling steps and loading both unchanged raw data files and transformed, prepared databases into new S3 folders.

#### 08_local_visualisations_notebook.ipynb:
Subsequently, the data can be analyzed either using AWS Glue crawlers and AWS Athena queries or locally, as demonstrated in the first half of the 08_local_visualisations notebook.ipynb, using tools like Jupyter Notebook or VSCode. The visualizations executed with these can be seen in the second half of the 08_local_visualisations_notebook.ipynb and could be freely reproduced with the code and the database found in Chicago_taxi_dataset_2024_06_10-14.zip. To ensure the code runs swiftly and without modification, it is recommended to read the data source under the name "trips_full."
