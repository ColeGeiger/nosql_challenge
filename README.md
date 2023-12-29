Eat Safe, Love - UK Food Ratings Analysis

Overview
The UK Food Standards Agency provides hygiene ratings for various establishments across the United Kingdom. In response to a request from the editors of the food magazine "Eat Safe, Love," we have conducted an analysis of the ratings data to help their journalists and food critics focus on potential article topics. This readme outlines the steps taken to set up the database, update it based on specific requirements, and perform exploratory analysis.

Part 1: Database and Jupyter Notebook Set Up
Database Creation and Data Import:

Imported the data from the establishments.json file into a MongoDB database named uk_food and a collection named establishments.
Copied the terminal command used for data import into a markdown cell in the Jupyter Notebook.
Library Import and MongoDB Connection:

Imported the necessary libraries: PyMongo for MongoDB interaction and Pretty Print (pprint) for displaying data.
Created an instance of the Mongo Client.
Database Confirmation:

Listed the databases in MongoDB to confirm the existence of uk_food.
Listed the collections in the database to ensure that establishments is present.
Found and displayed one document in the establishments collection using find_one and pprint.
Assigned the establishments collection to a variable for further use.
Part 2: Update the Database
Modifications to the Database:

Added information for a new halal restaurant, "Penang Flavours," in Greenwich, which has not been rated yet.
Found and returned the BusinessTypeID for "Restaurant/Cafe/Canteen."
Updated the new restaurant with the obtained BusinessTypeID.
Checked the number of documents containing the Dover Local Authority and removed establishments within the Dover Local Authority.
Data Type Conversion:

Used update_many to convert latitude and longitude to decimal numbers.
Used update_many to convert RatingValue to integer numbers.
Part 3: Exploratory Analysis
Performed an exploratory analysis to answer specific questions provided by "Eat Safe, Love":

Establishments with Hygiene Score 20:

Displayed establishments with a hygiene score equal to 20, including count, the first document, and a Pandas DataFrame.
High-Rated Establishments in London:

Displayed establishments in London with a RatingValue greater than or equal to 4, including count, the first document, and a Pandas DataFrame.
