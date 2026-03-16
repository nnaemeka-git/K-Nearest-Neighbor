# Custom k-Nearest Neighbors Classifier with Multiple Similarity Measures


This project demonstrates a custom implementation of the k-Nearest Neighbors (kNN) algorithm using a variety of similarity measures. The data set values are attributes of different wines from wine review. A one(1) indicates the presence of an attribute while a zero represent the absence of the attribute. Because of the size of the data set, the program utilized only a subset of the data set because of the time complexity of running the code on entire data set.
Instead of relying solely on standard Euclidean distance, this implementation supports five different similarity metrics:

•	Russell–Rao Similarity

•	Correlation Similarity

•	Jaccard Similarity

•	Rogers–Tanimoto Similarity

•	Yule Similarity

The goal is to classify scores into two categories:

•	Scores ≥ 90 → class (90 and above)

•	Scores < 90 → class (below 90)

By experimenting with multiple similarity measures, this project demonstrates how the choice of distance metric affects classification results, accuracy, precision, recall, and F1-score.
To run the codes on the entire data set, delete line 19 of the projects' code

# How It Works

## 1.	Data Preprocessing

o	Loads nb_score.csv.

o	Subsets the dataset (first 100 rows used for demonstration).

o	Converts scores into binary classes (above 90 and below 90).

# 2.	Similarity Measures Implemented

o	Russell–Rao: Based on joint presences of 1.

o	Correlation: Measures linear relationship between two vectors.

o	Jaccard: Ratio of shared features to the union of features.

o	Rogers–Tanimoto: Penalizes mismatches, extends Sokal & Michener.

o	Yule: Considers concordant vs. discordant pairs in binary data.

# 3.	Neighbor Selection

o	For each test record, compute similarity to all training records.

o	Sort similarities in descending order.

o	Select the top-k nearest neighbors.

# 4.	Prediction

o	Uses majority voting among neighbors’ labels.

# 5.	Evaluation
   
o	Outputs a confusion matrix (TP, FP, TN, FN).

o	Computes Accuracy, Precision, Recall, F1-score.

o	Runs experiments with different values of k and different similarity measures

