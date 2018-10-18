# Data 512 A Assignment 1 - Data curation

## Goal 

- Collect, analyze and publish a dataset of monthly traffic on the English Wikipedia between December 2007 and September 2018. 

## Outputs

- Link to the Jupyter Notebook :  [Jupyter notebook](https://github.com/lohithbruw/DATA512A/blob/master/data-512-a1/hcds-a1-data-curation.ipynb) 
- output files :   
    * en-wikipedia_traffic_200712-201809.csv
    * pagecounts_desktop-site_200712-201607.json
    * pagecounts_mobile-site_200712-201607.json
    * pageviews_desktop-site_201507-201809.json
    * pageviews_mobile-app-site_201507-201809.json
    * pageviews_mobile-web-site_201507-201809.json

## License
- License information for the source data can be found here [https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions]

## APIs Used for Data Collection

- Wikimedia Legacy Pagecounts API : [https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts)
- Wikimedia Pageviews API : [https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)

## Note
- Traffic from non user agents ie. crawlers, spiders etc are filtered from the Page Views data

## Cleaned/Aggregated Data

The final data is stored in a csv file : [https://github.com/lohithbruw/DATA512A/blob/master/data-512-a1/en-wikipedia_traffic_200712-201809.csv] with the following headers

| Column | Value | 
| ------ | ------ |
| year | year in the format YYYY | 
| month | month in the format MM | 
|pagecount_all_views| number of pagecounts : from Legacy API   |
|pagecount_desktop_views | number of pagecounts : from Legacy API  |
|pagecount_mobile_views	| number of pagecounts : from Legacy API  |
|pageview_all_views| number of Page views : from pageview API  |
|pageview_desktop_views| number of Page views : from pageview API|
|pageview_mobile_views| number of  Page views : from pageview API|


## Final Results 

The final visualization can be found here 

![Wikipedia Page Views Monthly between 2007 and 2018](https://github.com/lohithbruw/DATA512A/blob/master/data-512-a1/visualization.png)