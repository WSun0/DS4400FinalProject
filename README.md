# Music Genre Classification & Recommendation System

Final project for DS4400 - Machine Learning & Data Mining

## What it does

This project builds a system that:
- **Classifies songs into genres** using audio features (danceability, energy, tempo, etc.)
- **Recommends similar songs** based on audio similarity

We tested two models:
- **Logistic Regression** (baseline) - ~57% accuracy
- **Random Forest** (main model) - ~67% accuracy

The recommender uses Random Forest to predict genre, then finds similar songs within that genre using cosine similarity.

## Dataset

Uses Spotify-style audio features from `data_w_genres.csv`:
- 28,680 songs total
- Filtered to top 12 genres (2,740 songs) for better class balance
- Features include: danceability, energy, valence, acousticness, tempo, loudness, etc.

## Files

- `finalproject.ipynb` - Main notebook with all the code
- `data_w_genres.csv` - Main dataset with audio features and genres
- Other CSV files - Additional data splits (by artist, genre, year)

## Results

- **Random Forest** outperformed Logistic Regression by ~16% on both accuracy and F1-score
- **Recommender** achieved 0.86 average cosine similarity vs 0.29 for random same-genre songs
- Most important features: speechiness, acousticness, popularity

## Authors

Kaelynn Lackey & Will Sun
