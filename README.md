# Cyclistic Case Study!

Welcome to my Case Study on the fictional bikeshare company, Cyclistic! This was my capstone project for the Google Data Analytics Professional Certificate course. Thank you so much for stopping by and for any feedback given to me, both good and bad. I'm on a journey to improve and learn as much as I can so any feedback is greatly appreciated!

## The Source Data

The first order of business is to ensure access to the data that was used and all of my queries so if you want to inspect, manipulate or replicate my code you can do so easily! However, please keep the [Data License Agreement](https://ride.divvybikes.com/data-license-agreement) in mind when dealing with any of this data, or data related to this project.

The data files themselves were too large to upload directly to GitHub so instead I compressed them into a zip file and uploaded them [here](https://www.dropbox.com/s/45vltwmgyrfnum4/SourceData.zip?dl=0). You simply need to download a decompressing software such as, but not limited to, [WinRAR](https://www.win-rar.com/start.html?&L=0) to unzip the files to be able to access them.

## The Process

I then took the data that was in the "Trips" folder and imported it into my local [SSMS](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16) where I will be able to further inspect, and manipulate, the data to allow myself to analyze it properly using SQL queries. I simply created a database for the CaseStudy and then right click > Tasks > Import Data... and followed the prompts to import it into the correct server. Beware, it could take a very long time to import such large data sets, I treated it like a slow cooked stew; set it and forget it!

Once all of the data has been imported you can then start creating your tables and querying the data to answer whatever questions you are asking. For this next part please reference the files in this GitHub Project to see the steps I took in the appropriate order;

1. CreateTable.sql
2. UpdateSetTable.sql
3. DurationQuery.sql

For you, you might have to change the "FROM" clause in the query to match the appropriate location in your local database that you created. **Step 1** does most of the heavy lifting for your code as this is the large chunk of code that will create the table where you will aggregate all of the imported data. It will then select, transform and insert the data with the appropriate cleaned parameters (such as splitting the original "started_at" timestamp into 4 seperate StartDay, StartTime, StartMonth and StartDate datapoints) into the table we just created. While cleaning the data I noticed there was an error with the data where a few files had extra characters that was causing issues with conversion between data types. To rememdy this I performed **Step 2** which updated the table by removing the unnecessary characters. The final step was to utilize **Step 3** to create our final vital piece of data, Duration!

Voila! Just like that our data has been extracted, cleaned and transformed!
