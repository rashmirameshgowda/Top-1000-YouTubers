
# Top 1000 YouTubers Analysis

## POWER BI, POWER QUERY, DAX

Report built to analyse the Top 1000 YouTubers Dataset. 

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file. Transformations performed on the dataset in Power Query.
- Step 2 : Combined date, month and year columns to form a single date column. Removed date, month and year column.
- Step 3 : Replaced 'nan' values appropriately.
- Step 4 : Updated the data type of each column.
- Step 5 : Added calculated column - Avg Views per Upload.
- Step 6 : Set the wallpaper and theme as needed.
- Step 7 : Inserted icon, title bar, navigation buttons and filters for the report. 
- Step 8 : Created each visuals as per the business requirement.

### Page.1 of the report : Overview.

This page has important filters and scorecards with information about the important features in the dataset.

![Overview](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/b7495ba9-af8e-4288-9c47-8af992b806cb)

### Page.2 of the report : Top 10 Performers.

This page gives us more information about Top 10 YouTubers by Subscribers and Views. Top 10 Countries by Count of YouTubers and Avg views per upload.

![Top 10 Performers](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/01d39ce8-a91b-4546-8146-254978d184fa)

### Page.3 of the report : Core Elements.

This page has interesting information about correlations and if any parameter has affected YouTube Content Creation and the audience.

![Core Elements](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/bea1ff11-13ea-43b0-96da-3463e5b63448)

### Page.4 of the report : Geo.

Subscribers and Viewers accross Globe.

![GEO](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/0bcaa045-afe6-43a4-8702-6d8d7281a475)

### Key Insights.

1. T-Series stands first with highest number of subscribers and in the most viewed channel category.

2. United States stands first with more number of YouTubers and with the most number of views per upload.

3. Music, Sports & Education Channels have subscriber ratio more than the Youtubers ratio. This could be an indication that there is scope for gaining subscribers in this category.

4. With good number of Youtubers, 'Howto' category still lacks Subscribers.

5. Mr.Beast is the most recent popular YouTuber with 8million subscribers in the last 30days.

6. It's interesting to know that there is no positive correlation between total Youtuber count v unemployment rate and Youtuber count v tertiary enrolment rate.

7. Another interesting fact is that there is no positive correlation between the average population of a country v YouTuber count and Subscribers.


### Key Insights with Explanation.

1. T-Series stands first with highest number of subscribers and in the most viewed channel category.
![T-Series_1st](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/1121afc1-6349-4c30-94c0-8efcc03ecb4c)

2. United States stands first with more number of YouTubers and with the most number of views per upload.
![US_1st](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/18b2bd20-ff8b-4226-bc1f-ab91e34dbbd3)

3. Music, Sports & Education Channels have subscriber ratio more than the Youtubers ratio. This could be an indication that there is scope for gaining subscribers in this category.
![Subscribers v Youtubers](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/6b1e1498-3113-4b4f-bace-cdb8cab56bad)

4. With good number of Youtubers, 'Howto' category still lacks Subscribers.
![Howto](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/712a2db4-ee10-4be4-a478-be0dbb7de5aa)

5. Mr.Beast is the most recent popular YouTuber with 8million subscribers in the last 30days.

![last 30days subs](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/30e53bdd-036e-4394-8b73-e3ed4a49c721)

6. It's interesting to know that there is no positive correlation between total Youtuber count v unemployment rate and Youtuber count v tertiary enrolment rate.

![unemployement_rate   tertiary enrolment rate](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/e7de90b8-df22-49be-993e-88d093177c31)

7. Another interesting fact is that there is no positive correlation between the average population of a country v YouTuber count and Subscribers.

![avg population](https://github.com/rashmirameshgowda/Top-1000-YouTubers/assets/153609997/74d86493-c4ad-4934-9bb2-43b07046e6f8)


### DAX
 
         Avg Views per Upload = DIVIDE('Top 1000 Youtubers'[video_views],'Top 1000 Youtubers'[uploads],0)

         Highest Paid Youtuber = TOPN(1, ALL('Top 1000 Youtubers'[Youtuber]), CALCULATE([Highest yearly earnings]))

         Highest Subscribed Youtuber = TOPN(1, ALL('Top 1000 Youtubers'[Youtuber]), CALCULATE([Highest Subscribers]))

         Highest Subscribers = MAX('Top 1000 Youtubers'[subscribers])

         Highest Subscribers in last 30days = MAX('Top 1000 Youtubers'[subscribers_for_last_30_days])

         Highest Uploaded Channel = TOPN(1, ALL('Top 1000 Youtubers'[Youtuber]), CALCULATE([Highest Uploads]))

         Highest Uploads = max('Top 1000 Youtubers'[uploads])

         Highest yearly earnings = MAX('Top 1000 Youtubers'[highest_yearly_earnings])

         Recent Most popular Youtuber = TOPN(1, ALL('Top 1000 Youtubers'[Youtuber]), CALCULATE('Top 1000 Youtubers'[Highest Subscribers in last 30days]))

 
