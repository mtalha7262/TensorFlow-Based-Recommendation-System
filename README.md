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
