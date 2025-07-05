# TensorFlow-Based-Recommendation-System
MovieLens 100K
====================================================
               Movie Recommendation System
====================================================


Project Type  : Deep Learning | Recommender System
Frameworks    : TensorFlow, Keras, TFRS
Data Source   : MovieLens 100K
Language      : Python
====================================================

1. PROJECT OVERVIEW
--------------------
This system recommends movies to users by learning their preferences
from historical rating data. It uses a deep collaborative filtering 
approach implemented via embedding layers in a custom Keras model.

2. DATA DESCRIPTION
--------------------
- Movie metadata is loaded via TensorFlow Datasets (`movielens/100k-movies`).
- User ratings are loaded from the MovieLens `u.data` file with the columns:
    userId, movieId, rating, timestamp

- Genre mapping is performed for interpretability.
3. PREPROCESSING STEPS
------------------------
- Movie IDs and Titles are decoded and converted.
- Ratings are normalized to [0, 1] range.
- User and Movie IDs are encoded using index mapping.
- Ratings are split into training (90%) and validation (10%) sets.

4. MODEL ARCHITECTURE
-----------------------
- A custom Keras model class `RecommenderNet` is implemented.
- Model contains:
    - User & Movie Embedding Layers
    - Bias Layers for Users and Movies
    - Dot product between user & movie vectors + bias
    - Output: Sigmoid activation (0 to 1 rating prediction)

5. MODEL TRAINING
-------------------
- Loss: Binary Crossentropy
- Optimizer: Adam
- Batch Size: 32
- Epochs: 10

6. EVALUATION METRICS
-----------------------
- Accuracy
- Precision
- Recall

7. RECOMMENDATION STRATEGY
----------------------------
- Randomly selects a user
- Predicts ratings for all unseen movies
- Returns top 10 movies with highest predicted ratings



