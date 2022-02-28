# KickStarter_Analysis

## Overview Of Project

This Data set contains different type of Campaigns with their goal and pledge amounts with their outcomes which was held in different countries. ALso, Lousie's Play **FEVER** came close to its fundraising goal in short amount of time.

By organizing, sorting and analyzing a crowdfunding dataset, Lousie will be able to specify different factors that will make her campaign successful. 

### Purpose

The purpose of this project is to is to compare the results of fundraising campaigns based on their launch dates and their funding goals as well as the pledged amounts. In this dataset Lousie specifically looked at the trends of Theaters(category) to determine the successful, failed, and cancelled campaigns with respect to time of the year by months.

## Analysis And Challenges

### Analysis:

Before heading directly into the analysis, we can see that the dataset provided is organized by many different aspects such as Names of Campaigns, Blurbs, Goals, Pledgeds, Outcomes, Countries, Currencies, Deadlines, Launch Dates, Backers counts, categories. But, most of the dataset is analyzed by using filters and mostly in theater category and play subcategory.

#### Analysis Of Outcome Based On Lauch Date

For this Analysis, I have created pivot table by filtering Parent Category and years (Parent category and years column had to be added seperately in Kickstater sheet). Column field was filtered with outcomes in decending order while the rows were filtered in Date created Conversions in months wise.

<img width="718" alt="Theater Outcomes" src="https://user-images.githubusercontent.com/94248676/155907802-81279ecd-e992-4354-923c-9330dd77b3ad.png">

#### Analysis of Outcomes Based on Goals

To analyze this dataset, I made a coulmn range starting from Less than $10,000 until greater than $50,000 on increment of 5000 on each row. In order to receive corrent count I have used COUNTIFS function. This function will be useful to get us exact number for successful, failed and canceled events for plays in Subcategory. Moreover, after getting data's in that columns I found percentages of each coulmns by dividing each with subtotal with overall data.

<img width="953" alt="Outcomes based on Goals" src="https://user-images.githubusercontent.com/94248676/155907738-41fdb819-465d-4a5c-bf81-528fc8e36e8b.png">

### Challenges Encountered:

1) In Kickstarter Sheet the "Date Created Conversion" & "Date End Conversions" contained Unix TImestamps. It took me time to understand that data and convert it into human readable format. I have used "=(((J2/60)/60)/24)+DATE(1970,1,1)" forumula to convert it.

2) In sheet Theater Outcome by Launch Date, column was displayed in years format instead of months. It took me almost hour to figure it out that hpw will I convert it to month from Years & Quaters. Solution was very easy I just had to drag and drop years & quaerter out of pivot table field.

3) Using COUNTIFS function could be cucumbersome for the first couple of times. If you read instructions in formula tab under insert functions, you will never make a mistake and if someone still make mistake the it will be easier for that person to find his/her own mistakes. 

## Results

### Outcome based on Categories 

#### 1) Outcomes Based on Launch Dates:

Upon exploration of the data its seems that starting March until September, May is a most flourishing time of year for a theater campaign. Between March and May, the prospect is alomst more than a double but quickly tapers down from May on with a minor elevation from September to October. Its Facinating that the failure rate is also duplicating with the success trend but statistically at a much lower rate.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/94248676/155907829-f1256451-7256-4b80-b43a-38d50abbc6c1.png)

#### 2) Outcome Based on Goals:

Although the pattern fluctuates, it is apparent that play campaigns with higher goals tend to have a greater percent chance of failing. However, surprisingly the goal of $35,000 - $45,000 has a success rate of around 70%. The funding Goal of Less than $1,000 has the highest success rate of around 75%%, followed closely by the $1,000-$5,000 funding goal, with a success rate of around 73%.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/94248676/155907845-99aa464b-0aa0-4fbc-ace5-691ec0f26815.png)

### What are some limitations of this dataset?
Some limitations are:

1) The dataset I'm using is old as its data from year 2014-2016, and right now we are in 2022. So, the more recent data we have there are more chances of most relevant analysis. Also we do not have data from unexpected situtions which could totally make campaigns unsuccessful.

2) We have few outliers within the dataset and without further analysis we are unable to find the cause pf that outlier.

### Other Possible Tables and Graphs

1) We could add possible graphs of Box and Whiskers plots for the outliers.

2) We have just analyze one country US, but we could analyze more countries to distingush between the catogeries.









