# Clustering Analysis of Coaching Institute Question Bank Dataset

## Project Overview

This project analyzes a dataset from a coaching institute’s question bank, categorizing questions based on their difficulty levels (Easy, Medium, and Hard). The goal is to optimize practice sessions by identifying patterns and clusters related to question difficulty, time taken to solve, and average scores achieved.

## Dataset Description

The dataset contains several features related to student performance and time spent on answering questions. The key columns in the dataset are:

- **Average_Score**: The average score of students for each question.
- **Time_Taken**: The time (in seconds) it took to answer each question.
- **Attempt_Rate**: The attempt rate of students, representing the percentage of students who attempted the question.
- **Cluster_Level**: The difficulty level assigned to each question: Easy, Medium, Hard.

### Sample Data

| Average_Score | Time_Taken | Attempt_Rate | Cluster_Level |
|----------------|------------|--------------|---------------|
| 70             | 150        | 0.8          | Medium        |
| 80             | 180        | 0.9          | Hard          |
| 50             | 120        | 0.6          | Easy          |
| 65             | 100        | 0.7          | Medium        |
| 85             | 160        | 0.95         | Hard          |

## Data Preprocessing

- **Standardization**: All numerical features were standardized using `StandardScaler` to bring them to the same scale. This is essential for clustering algorithms like K-Means.
- **Label Encoding**: The categorical feature `Cluster_Level` was encoded using `LabelEncoder` for analysis purposes.
- **Clustering**: The data was grouped into clusters using the **K-Means** algorithm to identify patterns in question difficulty based on performance and time.
- **Principal Component Analysis (PCA)**: PCA was used to reduce the data to two dimensions for visualization purposes, helping to display clusters effectively.

## Clustering Visualization

Clusters were visualized in a scatter plot, showing the relationship between the scaled `Average_Score` and `Time_Taken`. The following colors represent different clusters:

- **Green**: Easy
- **Blue**: Medium
- **Purple**: Hard

The plot demonstrates the distribution of questions based on difficulty levels, helping to optimize the practice sessions by focusing on areas that may need more attention.

## Tools and Libraries Used

- **Python**: Programming language used for data analysis.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical operations on the dataset.
- **Matplotlib**: Data visualization.
- **Scikit-learn**: Machine learning tools, including K-Means for clustering, `LabelEncoder` for encoding categorical data, and `StandardScaler` for standardization.
- **PCA**: For dimensionality reduction and visualization of the clusters.
