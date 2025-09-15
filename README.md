# Iris Dataset Clustering Using K-Means
This repository contains an unsupervised machine learning project that identifies the optimal number of clusters in the famous Iris dataset and visualizes them. It's implemented in Python using scikit-learn for K-Means clustering. This was developed as part of The Sparks Foundation GRIP internship in Data Science and Business Analytics.

# Project Overview
The goal is to apply clustering techniques to group Iris flower species based on sepal and petal measurements, without using labels initially. We determine the best number of clusters using the elbow method and then visualize the results. This serves as an introductory example of unsupervised learning and dimensionality reduction.

# Key features:

Data loading and preprocessing

Exploratory data analysis with visualizations

Elbow method for optimal K

K-Means clustering and visualization

# Objective
From the given Iris dataset, predict the optimum number of clusters (expected to be 3, corresponding to the species) and represent it visually using scatter plots.

# Dataset
The dataset is the standard Iris CSV (included as Iris.csv). It consists of 150 samples from three species: Setosa, Versicolor, and Virginica. Columns include:

Id: Unique identifier (dropped during analysis)

SepalLengthCm: Sepal length in cm

SepalWidthCm: Sepal width in cm

PetalLengthCm: Petal length in cm

PetalWidthCm: Petal width in cm

Species: Target label (used for validation, not training)

Sample data preview:

SepalLengthCm	SepalWidthCm	PetalLengthCm	PetalWidthCm	Species
5.1	3.5	1.4	0.2	Iris-setosa
4.9	3.0	1.4	0.2	Iris-setosa
4.7	3.2	1.3	0.2	Iris-setosa
...	...	...	...	...
Total records: 150

Mean sepal length: ~5.84 cm

## Correlations: Strong positive between petal length/width (~0.96)

This dataset is a classic for ML benchmarking, sourced from UCI Machine Learning Repository.

# Methodology
Data Import: Load the CSV using pandas.

Exploratory Data Analysis (EDA):

Display head, tail, and summary statistics.

Compute correlations and visualize with heatmaps using seaborn.

Drop unnecessary 'Id' column.

Finding Optimal Clusters:

Use elbow method: Compute Within-Cluster Sum of Squares (WSS) for K=1 to 10.

Plot elbow curve to identify the 'elbow' point (typically K=3).

# Clustering:

Apply K-Means with optimal K.

Assign cluster labels to data points.

# Visualization:

Scatter plots of clusters (e.g., Sepal Length vs. Width, colored by cluster).

Compare with actual species for validation.

The notebook (TASK_2.ipynb) walks through these steps with code and outputs.

# Results
Optimal clusters: 3 (via elbow method).

Clusters correspond closely to the three Iris species.

Visualization shows clear separation, especially in petal dimensions.

Evaluation: Silhouette score or visual inspection confirms good clustering.

# How to Run
Clone this repository: git clone https://github.com/yourusername/iris-clustering.git

# Install dependencies: pip install -r requirements.txt

# Open Jupyter: jupyter notebook TASK_2.ipynb

Run all cells to see the analysis, elbow plot, and cluster visualizations.

# Requirements
### Listed in requirements.txt:

Python 3.x

numpy

pandas

matplotlib

seaborn

scikit-learn

# Limitations
Assumes clusters are spherical (K-Means limitation); may not handle complex shapes.

Small dataset; results are for demonstration.

No hyperparameter tuning beyond elbow method.

# Author
Manadip Sutradhar
MSc Chemistry Student, IIT Guwahati
Interests: Computational chemistry, ML applications, geochemical modeling

Feel free to fork or contribute! If you use this for your projects, credit is appreciated.
