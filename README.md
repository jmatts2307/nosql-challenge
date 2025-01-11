# nosql-challenge

In this challenge, there was an evaluation conducted on the ratings of various establishments across the United Kingdom.
For the initial set up, MongoDB was used to store data that was imported from the 'establishments.json' file that was located in the starter files. The database was named 'uk_food' and the collection was named 'establishments'. 
When importing the data, be sure to access the 'Resources' folder from terminal, and use: mongoimport --db uk_food --collection establishments --drop --file establishments.json --jsonArray

An instance of the MongoClient was created, and the databases were listed along with the collections, and it was confirmed that 'uk_food' and 'establishments' were listed and present in the database. 

Updating the database:
Using the 'NoSQL_setup_starter.ipynb', there was a new halal restaurant that was added to the database called 'Penang Flavours'. 
The new restaurant's 'BusinessTypeID' was updated. The magazine that the evaluations were being conducted for was not interested in any establishments in 'Dover', so there was a check conducted to see how many documents contained 'Dover Local Authority'. It was found that 994 establishments from 'Dover' existed, so they were removed from the database. 

Exploratory Analysis:
The magazine "Eat Safe, Love" had these specific questions that were analyzed and answered:
1. Which establishments have a hygiene score equal to 20?
The number  of establishments with a hygiene score of 20 is 41.
The results were converted into a Pandas DataFrame and can be viewed in the attached Jupyter Notebook. 

2. Which establishments in London have a RatingValue greater than or equal to 4?
The number of establishments in London with the RatingValue greater than or equal to 4 is 33. 
The results were converted into a Pandas DataFrame and can be viewed in the attached Jupyter Notebook.

3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
The top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant 'Penang Flavours' are: "Howe and Co Fish and Chips - Van 17", "Lumbini Grocery Ltd T/A Al-Iman", "Atlantic Fish Bar", "Iceland", and "Volunteer". 
The results were converted into a Pandas DataFrame and can be viewed in the attached Jupyter Notebook.

4. How many establishments in each Local Authority area have a hygiene score of 0?
The number of Local Authorities with a hygiene score of 0 is 55. 
The results were converted into a Pandas DataFrame and can be viewed in the attached Jupyter Notebook.
