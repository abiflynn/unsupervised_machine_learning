# Unsupervised Machine Learning: Creating Playlists

## 1. Project Objectives & Overview

### 1.1. Business Problem

Moosic is a little start up that creates curated playlists done by music experts and specialists in old and new trends. Users can subscribe to their website and listen to these playlists through their preferred Music App (be it Spotify, Apple Music, Youtube Music…). They love the fact that their playlists have a personal touch, and that each playlist encapsulates a certain “mood” or “style”.

But business is scaling up fast and the music experts are slow in creating new playlists. My mission is to use Data Science to add automatisation to the creation of playlists. I will use a dataset that has been collected from the Spotify API and contains the audio features (tempo, energy, danceability…) for a few thousand songs, and use a clustering algorithm such as K-Means to divide the dataset into a few clusters (which will become playlists).

The outcome of this project will be an initial prototype. 

### 1.2. Technical Skills

- Python
- Pandas
- Scikit-learn
- KMeans
- Matplotlib
- Seaborn 

## 2. Project Outcome

### 2.1. Findings

**The Dataset**
- Dataset with approx. 5200 songs to cluster into various playlists.
- After reviewing the data, we decided to drop the following columns:id, html, artist, type, key, mode, time_signature and duration_ms.

**Scaling**
- Decided to use the MinMaxScaler: 
<img width="590" alt="Screenshot 2023-04-20 at 22 52 48" src="https://user-images.githubusercontent.com/120720780/233495577-df23f8ee-6a0b-49d4-ab3e-1739f907cd09.png">

**Number of Clusters**
- Combining the findings of the Elbow chart with Inertia and the Silhouette Score I decided to go with 12 clusters / playlists.

<img width="431" alt="Screenshot 2023-04-20 at 22 55 28" src="https://user-images.githubusercontent.com/120720780/233495922-7b6abb3f-84b1-4204-9d91-ca316a1a9365.png">

**Qualitative Analysis**
- I conducted a comprehensive qualitative analysis and to review the results of the clusters/ playlists. 

<img width="513" alt="Screenshot 2023-04-20 at 23 00 19" src="https://user-images.githubusercontent.com/120720780/233496640-a9ec888d-defb-4961-9197-63ab31a68a77.png">

### 2.2. Summary 

- KMeans was able to cluster with decent efficiency for some of the values
- For other values, there was no consistency in clustering
- There was a strong randomness

- There was no sense for some of the genre “borders”; most infamously one playlist was made up of mostly Death Metal & Electronic Music / Techno because of similarities in loudness, tempo and energy.

My recommendation is to keep the human factor strong for now in establishing playlists and look into more refined ML solutions for the future.




