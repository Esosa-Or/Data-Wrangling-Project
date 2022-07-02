# Data-Wrangling-Project
A data wrangling and analysis project carried out in partial fulfullment of the Udacity nanodegree

### Background
The goal of this project was to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. This involved working on three different datasets, which were gathered in various ways. 

### Data Wrangling
First, the WeRateDogs Twitter archive which contains basic tweet data for all 5000+ of their tweets which was provided as a downloaded file, an image prediction file containing a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images), and finally, a self-generated dataset created by querying the Twitter API with my Twitter developer account to gather valuable data on retweet and favorite count.

The data was gathered using a variety of methods; 
1.	pd.read_csv was used for reading the downloaded file into the python using pandas. 
2.	The requests library was used for gathering data programmatically from provided 
3.	The Tweepy library was used to query additional data via the Twitter API (tweet_json.txt)

Next, the data was assessed visually and programmatically using various pandas methods and functions. The visual and programmatic assessment revealed various quality and tidiness issues, such as: 

1.	Invalid names in the 'name' column of the archive_df. Specifically,there are a total of 109 lower-case entries which are invalid names (e.g 'a','an', 'actually', 'the'etc)
2.	Extraneous html tags in some columns
3.	Retweets/replies in the dataframe
4.	Incorrect datatypes
5.	Invalid entries
6.	Missing Data
7.	Outliers
8.	Untidy columns etc 

These quality and tidiness issues would impact the quality of analysis and so must be cleaned before any analysis work can be done. Data cleaning activities carried out included: 

•	Deleting retweets so that only original tweets would be included in the dataset
•	Changing datatypes to correct datatypes for ease of analysis
•	Dropping outliers from the analysis since they were few in number and would skew our analysis
•	Dropping null columns
•	Transforming long data to wide data using pd.melt
•	Merging datasets
The Define-Code-Test framework for data cleaning was very helpful in this process and enabled me to methodically work through the data cleaning process.
At the end of the process, I was enable to generate a cleaned data set and produce beautiful visualizations which revealed interesting insights about the We_rate_dogs archive.

