# Movies-ETL

## Completed Deliverables 
### 1. ETL_function_test
#### ETL_function_test does the following:
- An ETL function is written to read in the three data files.
- The function converts the Wikipedia JSON file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
- The function converts the Kaggle metadata file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.
- The function converts the MovieLens ratings data file to a Pandas DataFrame, and the DataFrame is displayed in the ETL_function_test.ipynb file.

### 2. ETL_clean_wiki_movies
#### The extraction and transformation of wiki movies data does the following:
- The TV shows are filtered out, and the wiki_movies_df DataFrame is created.
- A try-except block is used to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.
- The extraction and transformation of the Wikipedia data in the ETL function does the following.
    1. A list comprehension is used to keep columns with non-null values.
    2. The non-null box office data is converted to string values using the lambda and join functions.
    3. A regular expression is used to match the six elements of "form_one" of the box office data.
    4. A regular expression is used to match the three elements of "form_two" of the box office data.
    5. The following columns are cleaned in the Wikipedia DataFrame:
        - The box office column
        - The budget column
        - The release date column
        - The running time column
- The cleaned Wikipedia data is converted to a Pandas DataFrame, and the DataFrame is displayed in the ETL_clean_wiki_movies.ipynb file.

### 3. ETL_clean_kaggle_data
#### The extraction and transformation of the Kaggle metadata using the ETL function does the following:
- The Kaggle metadata is cleaned.
- The Wikipedia and Kaggle DataFrames are merged.
- The following is performed on the merged Wikipedia and Kaggle DataFrames to create the movies_df.
- Unnecessary columns are dropped.
- A function is used to fill in the missing Kaggle data.
- The movies_df DataFrame is filtered to keep specific columns.
- The movies_df DataFrame columns are renamed.
- The extraction and transformation of the MovieLens ratings data using the ETL function does the following:
- The ratings counts are cleaned.
- The movies_df DataFrame is merged with the cleaned ratings DataFrame to create the movies_with_ratings_df DataFrame.
- The empty values in the movies_with_ratings_df DataFrame are filled with “0”.
- The movies_with_ratings_df and the movies_df DataFrames are displayed in the ETL_clean_kaggle_data.ipynb file. (5 pt)

### 4. ETL_create_database
#### Create data base code executes the following requirements:
- The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database, as determined by the movies_query.png.
- The data from the MovieLens rating CSV file is added to the ratings table in the SQL database, as determined by the ratings_query.png.
- The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file.

### 5. Resources
Data Source: movies_metadata.csv; ratings.csv; wikipedia-movies.json

Software: Python 3.7.11 64-bit (conda); jupyter-notebook; PGAgmin v6.4
