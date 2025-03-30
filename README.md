# KNN-Based Movie Recommender Engine

This project builds a simple movie recommendation system using the K-Nearest Neighbors (KNN) algorithm in Python. It answers the question:

> **Given a movie's features (e.g., IMDB rating and genres), what are the 5 most similar movies in the dataset?**

---

## Objective

At a smaller scale, this project simulates how platforms like Netflix or Hulu recommend similar movies. We use a subset of IMDB data and apply a content-based filtering approach using the KNN algorithm to return the most similar movies based on numeric features.

---

## Data Source

The dataset includes 30 movies with the following features:

- **IMDB Rating** (numeric)
- **Genre flags** (Biography, Drama, Thriller, Comedy, Crime, Mystery, History)
- **Movie Name** (used for display)
- **Movie ID and Label** columns (dropped during preprocessing)

You can download the dataset [here](https://github.com/ArinB/MSBA-CA-/blob/main/CA05/movies_recommendation_data.csv) or use the .csv file provided in the notebook.

## Make sure to take these steps while running the file (as I did):
1. **Data Preprocessing**
   - Loaded the CSV file using `pandas`
   - Dropped non-feature columns (`Movie Name`, `Movie ID`, and `Label`)
   - Retained only the IMDB rating and genre flags for similarity analysis

2. **Creating the Feature Vector**
   - Manually constructed a feature vector for the movie "The Post":
     ```
     IMDB Rating = 7.2
     Biography = Yes, Drama = Yes, Thriller = No, Comedy = No,
     Crime = No, Mystery = No, History = Yes
     ```

3. **Fitting the KNN Model**
   - Used `sklearn.neighbors.NearestNeighbors` with `euclidean` distance
   - Fit the model on the cleaned feature matrix

4. **Finding Similar Movies**
   - Queried the model to return the 5 closest movies to "The Post"
   - Displayed titles and similarity scores (lower = more similar)

5. **Reusable Function**
   - Created a `recommend_movies()` function to reuse the logic for any input vector


## There is also an example output for reference at the end of my code 
