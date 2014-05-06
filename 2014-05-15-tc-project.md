---
layout: post
title: Tommie's Project 2014
description: The Secret of Compound Interest
tags: edav project 
---

### Introduction
Initially there were two project proposals in the beginning of semester. 

The first proposal was about discovering hidden relations among College Major, Employment Rate, and Housing Trend. Most people can understand the consequence of housing market when employment rate is increasing or decreasing. But the concept of Employment is vague in terms of ages or years of working experience. My hypothesis is - there can be a relation in the popularity of college major with housing trend and/or employment rate in following few years. 

My study began with reviewing data sources including U.S. Census Bureau, U.S. Bureau of Labor Statistics, Federal Housing Finance Agency, and multiple college admin websites. The problem started from the beginning. Not only data formats  not clean at all. Sometimes data can exist in image or any type of freetext format, but there was no single or managemable sorces to abstract usable information. 

After couple weeks of struggling, I realized that without doing hard data cleanup, manipulation, transformation, and calculation repeatedly, I'd not be  not be able to  decided to move on to second proposal.

For my first school-employee-housing project idea, after searching multiple database from the U.S. Census Bureau, U.S. Bureau of Labor Statistics, and Federal Housing Finance Agency, I feel there is no applicable dataset which can be used without doing hard data cleanup, manipulation and calculation iteratively. The process of preparing raw information may take much longer than expected. This will leave me little room for more interesting work in data exploration and visualization.

So moving on to the second project idea, the 4-4-3-3 investment strategy study, following is a brief summary about finding data source.
- [Yahoo Finance](http://finance.yahoo.com): this is one of the oldest and popular financial website around today. The information provided is comprehensive and free. Product ranking summary is available. The problem is that no single entry can be found to download all data at once. Writing a data scraper is required to retrieve fund information one by one. 
- [TD Ameritrade](http://research.tdameritrade.com/grid/public/mutualfunds/premierlist/premierlist.asp): the website was rebuilt couple years ago to be user friendly with a good deal of financial information. Under their data screening tool, multiple funds are displayed in the same place. But the build-in export function can only be used for the overview type of data, not for specific fund ranking information.  
- [Fidelity Investment](https://www.fidelity.com/mutual-funds/overview): many companies use Fidelity as their 401k provider. The research utility from the Fidelity website provides good summary and detail information. Although data scraping is still needed, time to retrieving information can be minimized. However the biggest issue is that the website does not provides full-scale ranking information. 
- [Morningstar](http://www.morningstar.com/Cover/Funds.aspx): I signed up for a basic account and took a look at the content of fund performance section. It turns out that majority of information from the website can also be retrieved from Yahoo Finance for free. Since I need to calculate fund ranking regardless, Yahoo Finance is a better choice for the project data source.  

### The Secret Revealed
    Funds ranked top quartile by recent yearly return of same type
    Funds ranked top quartile by last two, three, and five years return of same type
    Top one-third of funds from last six months return of same type
    Top one-third of funds from last three months return of same type

### Learn to Swim in the Deep Data Sea
Financial Data Explored:
Yahoo Finance - no straight solution to download needed performance data
TD Ameritrade - no data exporting function for fund ranking information
Fidelity Investment - does not provides full-scale ranking information
Morningstar - similar to Yahoo Finance
Market Watch - can download master fund list here

Data Munging:
Becutiful Soup 4.3.2
Python 3
Excel 2010
SQL 2012

### A Picture is Worth a Thousand Words
<img src="http://tc2680.github.io/assignment_0/predicted_mysql_usage.jpg" width ="600">

Here is my revised version using the motion library from Google Charts. Because there is no exact information about other type of database usage in the original slide, I measure angles and multiply them by the total sample size of 276 to estimate database ranking. You can see the [motion chart][link-demo] here.
<img src="http://tc2680.github.io/assignment_0/mysql_comparison.png" width ="600">


### Back to the Future
[To Do] I am interested in not only one but multiple types of database models in the market. I found a database ranking information from [here][link-03]. The website have various types of comparison matrix calculated from these parameters: number of mentions of the system on websites, general interest in the system, frequency of technical discussions about the system, number of job offers in which the system is mentioned, number of profiles in professional networks in which the system is mentioned, and relevance in social networks. For visualization, this [example][link-04] from Junkcharts provides a good direction for future work.




### The Story Came In The Right Time
[link-01]: http://image.slidesharecdn.com/mariadb-10-131217154438-phpapp02/95/slide-45-1024.jpg?cb=1387317230
[link-02]: http://flowingdata.com/visualize-this/
[link-03]: http://db-engines.com/en/ranking
[link-04]: http://junkcharts.typepad.com/.a/6a00d8341e992c53ef01a51184b1f8970c-pi
[link-demo]: http://tc2680.github.io/assignment_0/blogpost2_rev1.html

Recently I received a request to research and compare usage of open source database engines. I did not have much experience in this area except few toy practices in MySQL database. So I decided to look at MySQL first. After some initial studies, I came across a presentation about [Maria DB][link-01]. One of the slides from the presentation was trying to discuss future usage of MySQL. 

<img src="http://tc2680.github.io/assignment_0/predicted_mysql_usage.jpg" width ="600">

According to Nathan Yau, the author of [Visualize This][link-02], pie or donut chart should be simple, data needs to be organized, and don’t put too many wedges in one chart. Before looking for the data source, there are few things about the donut chart which are not clear to me:
* The chart is supposed to compare predicted DB usage between 2013 and 2018. So which side is for 2013, left or right?
* The original talk was about MariaDB. For comparison, I think percentage of usage should be presented for not only MySQL but also MariaDB.
* There are hundreds of different databases. Can we extend the concept of DB usage to other type of database?
 
### Revision 1
Here is my revised version using the motion library from Google Charts. Because there is no exact information about other type of database usage in the original slide, I measure angles and multiply them by the total sample size of 276 to estimate database ranking. You can see the [motion chart][link-demo] here.
<img src="http://tc2680.github.io/assignment_0/mysql_comparison.png" width ="600">
