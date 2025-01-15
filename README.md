# nosql-challenge
 # MongoDB Establishments Analysis

This repository contains two Jupyter Notebooks that demonstrate the use of MongoDB for data analysis with Python. The analysis focuses on a dataset of UK food establishments, leveraging PyMongo, Pandas, and Pretty Print for data exploration and manipulation. 

## Contents

### Notebook 1: Database Setup and Data Import
This notebook covers the initial steps for setting up the database and performing basic operations.

#### Key Steps:
1. **Data Import**:
   - The `establishments.json` file is imported into MongoDB using the `mongoimport` command.
   - Database: `uk_food`
   - Collection: `establishments`

2. **Database Connection**:
   - Connect to MongoDB using PyMongo.
   - Verify the successful creation of the database and collection.

3. **Data Update**:
   - Add a new restaurant, "Penang Flavours," to the collection.
   - Update fields like `BusinessTypeID` based on existing data.
   - Remove establishments from a specific region (e.g., "Dover").
   - Convert specific fields (e.g., `RatingValue`, `longitude`, and `latitude`) to appropriate data types.

4. **Verification**:
   - Check and confirm all updates using PyMongo queries and Pretty Print.

### Notebook 2: Exploratory Data Analysis
This notebook focuses on exploratory analysis of the dataset using MongoDB queries and Pandas for deeper insights.

#### Key Analyses:
1. **Establishments with a Hygiene Score of 20**:
   - Query and count the documents.
   - Convert results to a Pandas DataFrame and display insights.

2. **Establishments in London with High Ratings**:
   - Filter establishments in London with `RatingValue` >= 4.
   - Display results and analyze them in a Pandas DataFrame.

3. **Top 5 Establishments Near "Penang Flavours"**:
   - Query establishments with a `RatingValue` of 5, sorted by lowest hygiene score, and closest to "Penang Flavours."
   - Convert results to a Pandas DataFrame for visualization.

4. **Hygiene Score by Local Authority**:
   - Use aggregation pipelines to count establishments with a hygiene score of 0 by Local Authority.
   - Sort and visualize the results using Pandas.

## Tools and Technologies
- **MongoDB**: Database for storing and querying establishment data.
- **PyMongo**: Python library for interacting with MongoDB.
- **Pandas**: Data manipulation and analysis.
- **Pretty Print**: For clean and readable query output.

## Instructions
1. Ensure MongoDB is installed and running on `port 27017`.
2. Import the dataset:
   ```bash
   mongoimport --db uk_food --collection establishments --file establishments.json --jsonArray
