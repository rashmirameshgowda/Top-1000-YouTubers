# Top-1000-YouTubers
End to End analysis of the Top 1000 YouTubers dataset. Power BI, Power Query and DAX used.

# Top 1000 YouTubers Analysis

## POWER BI, POWER QUERY, DAX

This report is built to analyse the Top 1000 YouTubers Dataset. 

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file. Transformations performed on the dataset in Power Query.
- Step 2 : Combined date, month and year columns to form a single date column. Removed date, month and year column.
- Step 3 : Replaced 'nan' values appropriately.
- Step 4 : Updated the data type of each column.
- Step 5 : Added calculated column.
{Avg Views per Upload = DIVIDE('Top 1000 Youtubers'[video_views],'Top 1000 Youtubers'[uploads],0)}
- Step 6 : Set the wallpaper and theme as needed.
- Step 7 : Inserted icon, title bar and filters for the report. 
- Step 8 : Created each visuals as per the business requirement.

### Page.1 of the report : Overview.

This page has important filters and scorecards with information about the important features in the dataset.
