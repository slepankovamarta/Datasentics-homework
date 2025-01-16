[Project Summary: Basic KNN Book Recommendation System] https://github.com/slepankovamarta/the-git-rocks/blob/901ac98772a65f8586f77237e4becfda925b7c6d/Domaci%20ukol%20VACLAV.ipynb)

Project Overview

This project implements a basic Book Recommendation System using the K-Nearest Neighbors (KNN) algorithm. The goal is to recommend books to users based on similar average ratings rather than genre or content, using collaborative filtering techniques. The dataset used combines two data files: Ratings and Books. Although a third dataset, Users, was available, it was not utilized in this project but may be incorporated in the future for more personalized recommendations through customer segmentation (e.g., based on age or location).

Data Preparation

Ratings Dataset: Contains user ratings for various books.

Books Dataset: Contains book details like titles and authors.

The data was merged to associate each book with its corresponding average rating.

Since the dataset did not include categorical data such as book genres, recommendations were based solely on the similarity of average ratings rather than genre or content.

Models Implemented

1. First Model: KNN with Euclidean Distance

Model: knn_model = NearestNeighbors(n_neighbors=11, metric="euclidean")

Approach:

The pivot matrix was created with books as rows and users as columns, where values represent the average ratings.

The Euclidean distance metric was used to measure the similarity between books based on their ratings.

Recommended books were those with similar average ratings.

2. Second Model: KNN with Cosine Similarity and Popularity Threshold

Model: knn_model2 = NearestNeighbors(n_neighbors=11, metric="cosine", algorithm="brute")

Approach:

A pivot matrix was created similar to the first model.

A popularity threshold was introduced to filter out books with low ratings. Only top-rated books were considered for recommendations.

The cosine similarity metric was used, which is more effective for sparse data, as it measures the angle between rating vectors rather than their absolute difference.

This model focuses on recommending top-rated books, which are often more expensive and therefore prioritized for recommendations.
