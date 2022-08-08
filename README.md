# Movies-ETL
## Project Overview
The purpose of this project is to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. The challenge focuses on refactoring code from the class module to create one function that takes in three files and performs the ETL process by adding the data to a PostgreSQL database. 
## Summary
https://github.com/Bropell/Movies-ETL

- Deliverable 1 of the challenge involves writing an ETL function to read three data files (Wikipedia data, Kaggle metadata, and MovieLens rating data) and creates three separate DataFrames which is shown in https://github.com/Bropell/Movies-ETL/blob/main/ETL_function_test.ipynb. 

- Deliverable 2 involves extracting and transforming the Wikipedia data which is shown in https://github.com/Bropell/Movies-ETL/blob/main/ETL_clean_wiki_movies.ipynb. The clean movie function was copied over from the class module to clean the movie data and filter out tv shows. List comprehension and Regexs' were used to drop columns with null values and match elements with different forms of data. The final DataFrame output has only the required columns, in a clean, ordered format as seen in the image below.
![alt text](https://github.com/Bropell/Movies-ETL/blob/main/Resources/wiki_movies_df_clean.png)

- Deliverable 3 involves extracting and transforming the Kaggle data which is shown in https://github.com/Bropell/Movies-ETL/blob/main/ETL_clean_kaggle_data.ipynb. The Kaggle metadata DataFrame was merged with the Wikipedia movies DataFrame to create the movies_df DataFrame. The unnecessary columns were dropped and missing Kaggle data was filled in with zeros. The MovieLens rating data DataFrame was merged with the movies_df DataFrame to create the movies_with_ratings_df DataFrame which was also cleaned. This DataFrame can be seen in the image below.
![alt text](https://github.com/Bropell/Movies-ETL/blob/main/Resources/movies_with_ratings_df_clean.png)   

- Deliverable 4 involves creating the Movie database in PostgreSQL which is shown in https://github.com/Bropell/Movies-ETL/blob/main/ETL_create_database.ipynb. The database password was imported from the config file and a connection was established to the PostgreSQL database. The movies and ratings tables were added to the SQL database. Queries were run to confirm all of the rows for each table were present. These outputs can be seen in the images below. 
<p align="center">
  <img src="https://github.com/Bropell/Movies-ETL/blob/main/Resources/movies_query.png"/>
  <img src="https://github.com/Bropell/Movies-ETL/blob/main/Resources/ratings_query.png"/> 
</p>
