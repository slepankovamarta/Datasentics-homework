[Project Summary: Basic KNN Book Recommendation System](https://github.com/slepankovamarta/the-git-rocks/blob/901ac98772a65f8586f77237e4becfda925b7c6d/Domaci%20ukol%20VACLAV.ipynb)

Project Overview

I have implemented a basic Book Recommendation System using the KNN. The dataset used combines two data files: Ratings and Books. Dataset - Users - was available, it was not utilized in this project. In "Future Works" may be incorporated  through customer segmentation (but for example Age must be filled in)

Data Preparation
The data was merged with newly created average rating (because amount of IDs vary for each book).
Since the dataset did not include categorical data such as book genres, recommendations were based solely on the similarity of "Average- Ratings"


Models Implemented
1. First KNN Model with Euclidean Distance
(n_neighbors=11, metric="euclidean")
Recommended books were those with similar average ratings.

2. Second KNN Model with Cosine Similarity and Popularity Threshold
(n_neighbors=11, metric="cosine", algorithm="brute")
A popularity threshold to filter TOP books (only top-rated books were considered for recommendations ) meaning, the books that are regularly rated by users with higher score
Recommending top-rated books, which are often more e.g. expensive 
