# Data 512 A Assignment 2 - Bias in Data


## Goals
* Explore the concept of bias using data on Wikipedia articles on political figures from different countries.
* Generate table showing 10 highest-ranked countries in terms of number of politician articles as a proportion of country population
* Generate table showing 10 lowest-ranked countries in terms of number of politician articles as a proportion of country population
* Generate table showing 10 highest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country
* Generate table showing 10 lowest-ranked countries in terms of number of GA and FA-quality articles as a proportion of all articles about politicians from that country
* Reflect on this assignment on how this helps scientists understand the causes and consequences of bias on Wikipedia


## Analysis file 
* The Jupyter notebook containing the analysis can be found here : https://github.com/lohithbruw/DATA512A/blob/master/data-512-a2/hcds-a2-bias.ipynb

## Data sources used

* The Wikipedia dataset can be found here : https://figshare.com/articles/Untitled_Item/5513449
    * Wikipedia dataset contains the following columns:
        * page : Contains Page title
        * country : Contains Country names
        * rev_id :  contains the edit ID of the last edit to the page
* The population dataset can be found here : https://www.dropbox.com/s/5u7sy1xt7g0oi2c/WPDS_2018_data.csv?dl=0

## Resources used
* This analysis was performed in a "Python 3.6.5 :: Anaconda, Inc." environment 
* The following Python packages were used and their documentation can be found at the accompanying links:
** requests : http://docs.python-requests.org/en/master/
** json : https://docs.python.org/3/library/json.html
** pandas : https://pandas.pydata.org/pandas-docs/stable/
** numpy : https://docs.scipy.org/doc/

## Files Generated
* The CSV file that contains the combined data from wikipedia and ORES can be found here : https://github.com/lohithbruw/DATA512A/blob/master/data-512-a2/final_data.csv


## License Information

This project is released under MIT license. 
The License file can be found here : https://github.com/lohithbruw/DATA512A/blob/master/data-512-a2/LICENSE

## Reflections
* The reflections corresponding to each one of the tables generated in the analysis are provided within the notebook : https://github.com/lohithbruw/DATA512A/blob/master/data-512-a2/hcds-a2-bias.ipynb