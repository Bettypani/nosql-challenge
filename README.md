# nosql-challenge

Analysis of UK Food Standards Agency Data
This README file provides an overview of the steps taken to import, update, and analyze the UK Food Standards Agency data for Eat Safe, Love magazine. The analysis is performed using Python, MongoDB, and Jupyter Notebook.

Part 1: Database and Jupyter Notebook Set Up
Import Data
The data provided in the establishments.json file is imported into a MongoDB database named uk_food with a collection named establishments. The following command is used in the terminal: mongoimport --db uk_food --collection establishments --file establishments.json --jsonArray

Libraries and Client Setup
PyMongo and Pretty Print (pprint) libraries are imported.
An instance of the Mongo Client is created.
Confirming Data Import
The list of databases is obtained to confirm the existence of uk_food.
The list of collections in the uk_food database is obtained to confirm the existence of establishments.
A document from the establishments collection is retrieved and displayed using find_one along with pprint.
The establishments collection is assigned to a variable for further use.

Part 2: Update the Database
Modifications to the Database
A new restaurant, "Penang Flavours," in Greenwich, is added with a rating pending status.
The BusinessTypeID for "Restaurant/Cafe/Canteen" is found and updated for the new restaurant.
Establishments within the Dover Local Authority are removed from the database.
Number values stored as strings are converted to numeric values using update_many.

Part 3: Exploratory Analysis
Questions to Explore
Establishments with a hygiene score equal to 20.
Establishments in London with a RatingValue greater than or equal to 4.
Top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to "Penang Flavours."
Number of establishments in each Local Authority area with a hygiene score of 0, sorted from highest to lowest.
Additional Notes
RatingValue ranges from 1-5, with higher values indicating better ratings.
Hygiene, Structural, and ConfidenceInManagement scores work in reverse, where higher values indicate poorer performance.

Files Included
Jupyter Notebook: NoSQL_analysis_starter.ipynb
JSON file containing data: establishments.json





