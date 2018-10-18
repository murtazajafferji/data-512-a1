# DATA512 - A1: Data curation 

The goal of this project is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through September 30 2018 and exemplify best practices for open scientific research. All analysis is contained within the Jupyter notebook hcds-a1-data-curation.ipynb. 

### Curated Dataset

The dataset is a combination of monthly data from the Pageview API and Pagecount API to produce 130 records listed in ascending order based on date:

| Header                  | Description                                                                                                   |
|-------------------------|---------------------------------------------------------------------------------------------------------------|
| year                    | Year of timestamp in YYYY format                                                                              |
| month                   | Month of timestamp in MM format                                                                               |
| pageview_all_views      | Page view count obtained from Pageviews API for desktop, mobile-app, and mobile-web user traffic              |
| pageview_mobile_views   | Page view count obtained from Pageviews API for mobile-app and mobile-site traffic user traffic               |
| pageview_desktop_views  | Page view count obtained from Pageviews API for desktop user traffic                                          |
| pagecount_all_views     | Page view count obtained from Pagecount API for desktop-site and mobile-site user/spider/crawler traffic      |
| pagecount_desktop_views | Page view count obtained from Pagecount API for desktop-site user/spider/crawler traffic                      |
| pagecount_mobile_views  | Page view count obtained from Pagecount API for mobile-site user/spider/crawler traffic                       |

Filename: en-wikipedia_traffic_200801-201709.csv

### Visualizing the dataset

![alt text](https://github.com/murtazajafferji/data-512-a1/blob/master/en-wikipedia_traffic_200712-201809.png)

### Requirements

  - [Python 3.X](https://www.anaconda.com/download/)
  - [Jupyter](https://jupyter.org/install.html)
  - [Matplotlib](https://matplotlib.org)
  - [Pandas](http://pandas.pydata.org)

### Important notes

  - The Pageview API allows filtering by agent=user. However, the Pagecount API cannot differentiate between user traffic and traffic from web crawlers or spiders.

  - There is about 1 year of overlapping traffic data between the two APIs.

  - Start date is hardcoded as 200712 and end date is hardcoded as 201809, so as new data becomes available, these dates will need to be updated

  - A value of 0 in the dataset means that the traffic data was not available from the API for the given date

### Wikimedia REST API Documentation
This dataset included in this project is constructed using the Pagecounts API and the legacy Pageviews API.

*Pagecounts API* ([Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)) provides access to desktop and mobile traffic data from January 2008 through July 2016.

*Pageviews API* ([Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through September 2017.

### License 

By using Wikimedia REST API, you agree to Wikimedia's [Terms of Use](https://wikimediafoundation.org/wiki/Terms_of_Use/en) and [Privacy Policy](https://wikimediafoundation.org/wiki/Privacy_policy).

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/murtazajafferji/data-512-a1/blob/master/LICENSE) file for details
