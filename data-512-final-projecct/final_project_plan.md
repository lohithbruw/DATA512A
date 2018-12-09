# Final Project Plan - Analysis of OASDI Beneficiaries by State and ZIP Code, 2016
Author : Lohith B R  
Course Code : DATA 512   
University of Washington, Fall 2018

## Introduction

Social Security has become very important these days epecially in a developed country like the United States. Income derived from Social Security is currently estimated to have reduced the poverty rate for Americans age 65 or older from about 40% to below 10%.<sup>[1](https://www.cbpp.org/research/social-security/social-security-keeps-22-million-americans-out-of-poverty-a-state-by-state)</sup>. In 2018, the trustees of the Social Security Trust Fund reported that the program will become financially insolvent in the year 2034.<sup>[2](https://www.ssa.gov/oact/tr/2018/tr2018.pdf)</sup>. Thus it is very important that we analyze where the money is going and see if there are better ways to solve some of the problems instead of directly paying the beneficiaries. For e.g. it may be a good idea to invest more upgrading or reforming the health care system to reduce the cost of health care per person. It is also important to identify and prevent Social Security Fraud. This analysis can, in theory, help decision makers make informed decisions.

The annual publication of OASDI(Old-Age, Survivors & Disability Insurance) benefits from the Social Security Administration (SSA) presents the basic program data on the number and type of beneficiaries and the amount of benefits paid each state at the ZIP code level. This dataset also shows the number of men and women aged 65 or older receiving benefits. This dataset contains only those persons to whom the benefits are payable. Those whose benefits were withheld are excluded. 

This dataset will be used in this analysis to answer some of the research questions and also, if possible, uncover some interesting patterns/insights.


## Disclaimer about the Data <sup>[3](https://www.ssa.gov/policy/docs/statcomps/oasdi_zip/2016/oasdi_zip16.pdf)</sup>

The data in this report are derived from the Master Beneficiary Record, the principal administrative file of Social Security beneficiaries. The Social Security Detailed Office Organization Resource System (DOORS) file was used to associate the field office data with the ZIP Codes. Data for field offices in each state include only beneficiaries in that state. However, some Social Security field offices serve residents of more than one state. To obtain field office totals in these situations, it is necessary to combine data for each state served by the field office. The data include only persons whose benefits are currently payable. Those whose benefits were withheld are excluded.

Errors in the dataset will be updated by the SSA and can be viewed here : https://www.ssa.gov/policy/docs/statcomps/oasdi_zip/2016/index.html

## Anonymity <sup>[3](https://www.ssa.gov/policy/docs/statcomps/oasdi_zip/2016/oasdi_zip16.pdf)</sup>

To avoid disclosing the reason for Social Security eligibility of small groups and the amounts of benefits received, a controlled rounding procedure was used for field office and ZIP Code data. Data are not shown for ZIP Codes with fewer than 15 beneficiaries. Under the controlled rounding procedure, ZIP Code data on the number of beneficiaries shown in the table are changed according to the following formula:
1. If the number is divisible by 5 (ends in 0 or 5), then the numbers are not changed.
2. Otherwise, the number is rounded either to the next higher number divisible by 5 or the next lower number divisible by 5, in such a way that the difference between each rounded and unrounded cell value, each rounded and unrounded row total, and each rounded and unrounded column total is less than 5. The dollar amounts in the tables are rounded to the nearest thousand.


## Data

* Metadata for the dataset

|  Attribute | Value  |
|---|---|
|  Last Updated | December 2, 2017  |
|  Created |  December 2, 2017 |
|  File Format | MS Excel  |
|  License | [Creative Commons CCZero](https://creativecommons.org/publicdomain/zero/1.0/legalcode)  |
| Number of sheets  | 56  |
|  ID | 2d66781f-0590-4cee-95ea-d8ab01e08e03  |
| Revision ID | c745f739-adee-4936-b575-9cc44548e45a |
| Raw File Size | 3.4 MB|

* Every sheet either corresponds to a State or a territory in the US
* Every sheet has the following data format




|  Headers  |Data Type / Description   |
|---|---|
| Field Office and Zip Code  | Text(either field office name or ZIP code)  |
| Total  | Text(denoting a comma seperated number)  |
| Retired workers  |  Text(denoting a comma seperated number) |
| Disabled Workers  | Text(denoting a comma seperated number)  |
| Widow(er)s and parents  | Text(denoting a comma seperated number)  |
| Spouses | Text(denoting a comma seperated number)  |
| Children  | Text(denoting a comma seperated number)  |
| All Beneficiaries  | Text(denoting a comma separated number in terms of thousands of dollars)  |
| Retired Workers  |  Text(denoting a comma separated number in terms of thousands of dollars) |
| Widow(er)s and parents  | Text(denoting a comma separated number in terms of thousands of dollars)  |
| Number of OASDI beneficiaries aged 65 or older | Text(denoting a comma seperated number)  |

* If it turns out that I need more data from other sources, I will try to incorporate them during the analysis and quote the source.


## Research Questions
I am interested in answering the following questions

* What states/zip codes receive some of the highest/lowest amount of benefits?
* What states/zip codes have some of the highest/lowest number of people claiming benefits?
* Do all the zip codes in a given state receive similar amount of benefits, or are there states that have certain zip codes within them that receive a disproportionate amount of benefits as compared to other zip codes in the same state.
* Do huge-urban areas receive more benefits per eligible person than the rural areas? or is it the other way around? Is it different in different states?
* What does the distribution of people in the categories Retired workers, Disabled Workers, Widow(er)s and parents, Spouses and children look like for different states and which state has a highly skewed distribution


In addition to answering the questions above, I will try to uncover interesting patterns in the dataset, come up with additional questions that can be answered using the dataset etc.

## Analysis
* The first step in my Analysis will be to read the Excel files using the Pandas library
* The second step is to combine the dataset in different sheets into a more manageable datastructure, eg: Single dataframe
* Try to answer the research questions by using the filtering and aggregation operations using Pandas library
* Will try to use Matplotlib or Seaborn library to visualize data wherever appropriate
* If possible, I will try to perform some additional analysis to uncover strange patterns and this includes visualizing certain columns, filtering, joining etc.

## Tools

* I plan to use the python(3.x) programming language on a Jupyter Notebook
* I will be using the Matplotlib and/or the Seaborn Library to visualize data wherever appropriate
* Since the dataset is not really huge, I am planing to run the analysis on my computer instead of using the cloud
* I may also use Tableau for visualizing data if it feels like it's difficult to use Matplotlib

## Data Source Reference

* Background information about the program was obtained from this document on the Social Security Administration Website : https://www.ssa.gov/policy/docs/statcomps/oasdi_zip/2016/oasdi_zip16.pdf
* The dataset is downloaded form this page : https://catalog.data.gov/dataset/oasdi-beneficiaries-by-state-and-zip-code-2016

## Other Referenced Material
* [1] https://www.cbpp.org/research/social-security/social-security-keeps-22-million-americans-out-of-poverty-a-state-by-state
* [2] https://www.ssa.gov/oact/tr/2018/tr2018.pdf 
* [3] https://www.ssa.gov/policy/docs/statcomps/oasdi_zip/2016/oasdi_zip16.pdf

## Tools Documentation Sources

* https://docs.python.org/3/
* http://jupyter.org/
* https://pandas.pydata.org/pandas-docs/stable/
* https://matplotlib.org/contents.html
* https://seaborn.pydata.org/
* https://www.tableau.com/learn/training
* https://public.tableau.com/en-us/s/ 