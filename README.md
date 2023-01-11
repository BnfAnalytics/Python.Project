# Python.Project
Projects on Python using step-by-step process of industry
Data Cleaning of Google play Store Data Using Python-Pandas
Objective: Make the data clean for predictive model for Google Play Store. 
Problem Statement:
Google Play Store team is about to launch a new feature wherein, certain apps that are promising, are boosted in visibility. 
Domain: General
Analysis to be done: Using Data cleaning identify 
•	Clean Empty Cells
•	Clean Wrong Format
•	Clean Wrong Data
Content: Dataset: Google Play Store data (“googleplaystore.csv”)
Fields in the data –
•	App: Application name
•	Category: Category to which the app belongs 
•	Rating: Overall user rating of the app
•	Reviews: Number of user reviews for the app
•	Size: Size of the app
•	Installs: Number of user downloads/installs for the app
•	Type: Paid or Free
•	Price: Price of the app
•	Content Rating: Age group the app is targeted at - Children / Mature 21+ / Adult
•	Genres: An app can belong to multiple genres (apart from its main category). For example, a musical family game will belong to Music, Game, Family genres.
•	Last Updated: Date when the app was last updated on Play Store
•	Current Ver: Current version of the app available on Play Store
•	Android Ver: Minimum required Android version
 
Steps to perform:
1.	Load the data file using pandas. 
2.	Data Cleaning using python-pandas
a)	Clean Empty Cells
i.	Check for null values in the data. Get the number of null values for each column.
ii.	Drop records with nulls in any of the columns. 
b)	Clean Wrong Format
i.	Variables seem to have incorrect type and inconsistent formatting. You need to fix them: 
ii.	Size column has sizes in Kb as well as Mb. To analyze, you’ll need to convert these to numeric.
a.	Extract the numeric value from the column
b.	Multiply the value by 1,000, if size is mentioned in Mb
iii.	Reviews are a numeric field that is loaded as a string field. Convert it to numeric (int/float).
c)	Clean Wrong Data
i.	Variables seem to have incorrect type and inconsistent formatting. You need to fix them: 
ii.	Installs field is currently stored as string and has values like 1,000,000+. 
a.	Treat 1,000,000+ as 1,000,000
b.	remove ‘+’, ‘,’ from the field, convert it to integer
iii.	Price field is a string and has $ symbol. Remove ‘$’ sign, and convert it to numeric.
d)	Sanity checks:
i.	Average rating should be between 1 and 5 as only these values are allowed on the play store. Drop the rows that have a value outside this range.
ii.	Reviews should not be more than installs as only those who installed can review the app. If there are any such records, drop them.
iii.	For free apps (type = “Free”), the price should not be >0. Drop any such rows.
