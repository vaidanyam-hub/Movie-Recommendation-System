# Movie Recommendation System using Collaborative Filtering

## Project Overview

With the rapid growth of streaming platforms such as Netflix, Amazon Prime, and Disney+, users often struggle to find movies that match their interests. This project builds a personalized movie recommendation system using **Collaborative Filtering**, a technique widely used in modern recommendation engines.

The system analyzes user rating behavior and recommends movies based on similarities between users and movies.

---

## Objectives

* Build a personalized movie recommendation system
* Analyze user rating patterns
* Create a User-Item Rating Matrix
* Recommend Top-5 movies to users
* Evaluate recommendation performance using RMSE

---

## Dataset Information

The dataset contains movie ratings provided by users.

### Features

| Column  | Description                    |
| ------- | ------------------------------ |
| userId  | Unique User ID                 |
| movieId | Unique Movie ID                |
| rating  | Rating given by the user (1–5) |
| title   | Movie title                    |
| genre   | Movie category                 |

### Sample Data

| userId | movieId | rating | title         |
| ------ | ------- | ------ | ------------- |
| 1      | 5       | 4      | Titanic       |
| 2      | 3       | 5      | Interstellar  |
| 3      | 8       | 3      | Jurassic Park |

---

## Methodology

### 1. Data Preprocessing

* Loaded dataset using Pandas
* Removed missing values
* Prepared data for recommendation analysis

### 2. User-Item Matrix Creation

A User-Item Matrix was created where:

* Rows represent users
* Columns represent movies
* Values represent ratings

This matrix forms the foundation of collaborative filtering.

### 3. Similarity Calculation

Cosine Similarity was used to measure similarity between movies.

**Formula:**

Similarity = (A · B) / (||A|| × ||B||)

### 4. Collaborative Filtering

Implemented **Item-Based Collaborative Filtering** to recommend movies that are similar to movies previously liked by users.

### 5. Recommendation Generation

Generated Top-5 personalized recommendations for each user based on similarity scores and rating history.

### Example Recommendation

**User ID: 3**

1. Toy Story
2. Jumanji
3. Star Wars
4. Jurassic Park
5. Forrest Gump

---

## Model Evaluation

The recommendation system was evaluated using **Root Mean Square Error (RMSE)**.

### Formula

RMSE = √(1/n × Σ(y_predicted − y_actual)²)

### Result

| Metric | Value |
| ------ | ----- |
| RMSE   | 1.91  |

A lower RMSE indicates better prediction accuracy. The model achieved reasonable performance for the available dataset.

---

## Key Outcomes

* Built a User-Item Rating Matrix
* Implemented Item-Based Collaborative Filtering
* Calculated Movie Similarity using Cosine Similarity
* Generated Personalized Movie Recommendations
* Evaluated Recommendation Quality using RMSE
* Developed an End-to-End Recommendation System

---

## Challenges Faced

### Sparse Ratings

Many users had rated only a small subset of movies, resulting in sparse data.

### Cold Start Problem

New users without rating history could not receive accurate recommendations.

### Limited Dataset

Prediction quality was constrained by the size of the dataset.

---

## Future Improvements

* Implement Matrix Factorization (SVD)
* Build a Hybrid Recommendation System
* Add Genre-Based Recommendations
* Develop a Streamlit Web Application
* Scale to MovieLens 1M Dataset

---

## Tools & Technologies

| Category             | Technology              |
| -------------------- | ----------------------- |
| Programming Language | Python                  |
| Data Analysis        | Pandas, NumPy           |
| Machine Learning     | Scikit-Learn            |
| Similarity Technique | Cosine Similarity       |
| Evaluation Metric    | RMSE                    |
| Environment          | Google Colab            |
| Dataset              | MovieLens Style Dataset |

---

## Project Structure

```text
Movie-Recommendation-System/

├── movie_recommendation.ipynb
├── movie_recommendation_dataset.csv
└── README.md
```

## Conclusion

This project demonstrates how Collaborative Filtering can be used to build personalized recommendation systems. By analyzing user preferences and similarity patterns, the model successfully recommends relevant movies and provides a practical introduction to recommendation engine development.
