# Reinforcement Learning-Based Movie Recommendation System

This project implements a hybrid movie recommendation system that combines **Matrix Factorization** using **Singular Value Decomposition (SVD)** with **Q-learning**, a Reinforcement Learning (RL) approach. The system is trained and evaluated on the [MovieLens 100K dataset](https://grouplens.org/datasets/movielens/100k/).

---

## Features

- **Matrix Factorization (SVD):**
  - Uses collaborative filtering to generate user-item latent features.
  - Reconstructs user preferences based on historical ratings.

- **Reinforcement Learning (Q-Learning):**
  - Simulates user interactions to update a Q-table of user-movie values.
  - Learns personalized movie preferences based on simulated reward signals.

- **Evaluation:**
  - Root Mean Square Error (RMSE) on predicted ratings (SVD).
  - Average reward from the Q-learning agent on test data.

- **Interactive Frontend (via IPython Widgets):**
  - Enter a User ID to get top movie recommendations.
  - Compare results from SVD and Q-learning.

---

## Installation


pip install -r requirements.txt
Usage
Training and Evaluation

Run the notebook to:

Load and preprocess data.

Train the SVD model and compute predictions.

Train the Q-learning agent.

Save the trained models to disk (movie_recommendation_model.joblib).

Interactive Recommendations

Use the widget interface at the end of the notebook:

Input a User ID.

View top 5 recommendations from both SVD and Q-learning.

Key Differences in Recommendation Approaches
Aspect	SVD	Q-Learning
Type	Collaborative Filtering	Reinforcement Learning
Basis	Latent factors from ratings matrix	Simulated user feedback
Accuracy	Generally high	Dependent on reward design
Limitations	Cold start for new users/items	Can be unstable with poor simulation

The Q-learning model in this version relies on a basic simulated feedback function, which leads to recommendations that may not align closely with actual user preferences.

Example Output

Recommended Movies (SVD):
- Rear Window (1954)
- Chinatown (1974)
- Manchurian Candidate, The (1962)

Recommended Movies (Q-Learning):
- Power 98 (1995)
- Wonderland (1997)
- Midnight Dancers (Sibak) (1994)
The difference is due to the more data-driven approach of SVD versus the exploratory and simulated nature of Q-learning.

Dataset
MovieLens 100K: 100,000 ratings from 943 users on 1,682 movies.

Format: UserID, MovieID, Rating, Timestamp

Improvements
To improve the Q-learning component:

Use actual rating values in the reward function.

Extend state representation beyond just User ID.

Increase number of training episodes and improve exploration strategy.

Consider Deep Q-Learning for scalability.

#License


This project is intended for academic and research use.

