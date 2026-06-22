# Human Activity Clustering

![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?logo=python\&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Unsupervised-7C5CFF)
![Clustering](https://img.shields.io/badge/Task-Activity%20Clustering-orange)
![Feature Engineering](https://img.shields.io/badge/Feature%20Engineering-Time%20Series-purple)

## Overview

Modern wearable devices such as fitness trackers, smart watches, cameras, and motion sensors continuously collect information about human activity. These data can be used in many real-world applications, including healthcare monitoring, fitness tracking, navigation, safety control, and activity recognition.

In this project, sensor data collected from wearable devices are used to identify different types of human physical activity. The data include measurements from three IMU sensors and a heart rate monitor. Based on these signals, the task is to cluster observations into groups that may correspond to different activities, such as walking, running, sleeping, standing, or other movement patterns.

Since the task is based on clustering, the solution focuses on unsupervised machine learning methods and further interpretation of the obtained groups.

---

## Objective

The main objective of this project is to build a reproducible machine learning pipeline for clustering human activity data using wearable sensor measurements.

The solution includes:

* exploratory data analysis;
* data preprocessing;
* feature engineering for sensor and time-series data;
* feature selection and feature importance analysis;
* training and comparison of several clustering models;
* hyperparameter tuning;
* selection of the best model;
* prediction on test data;
* interpretation of the resulting clusters;
* preparation of a submission file for Kaggle.

---

## Dataset Description

The dataset contains measurements collected from wearable sensors:

* three inertial measurement units;
* heart rate sensor.

The data may include different types of signals, such as:

* acceleration;
* angular velocity;
* orientation-related measurements;
* heart rate values;
* time-dependent sensor features.

These signals describe user movement and physiological state. The main task is to identify hidden patterns in the data and group similar activity records together.

---

## Machine Learning Task

This is an **unsupervised learning** task.

The goal is to cluster sensor records into groups according to the type of activity. Since the true labels may not be directly available during model training, clustering algorithms are used to discover the internal structure of the data.

Possible activity groups may correspond to:

* walking;
* running;
* resting;
* sleeping;
* standing;
* sitting;
* other physical activity patterns.

---

## Project Pipeline

The full solution is organized as a structured machine learning pipeline.

### 1. Exploratory Data Analysis

At this stage, the dataset is analyzed to understand its structure and quality.

Main steps:

* checking dataset shape;
* analyzing feature types;
* checking missing values;
* studying distributions of sensor features;
* detecting outliers;
* analyzing correlations between features;
* visualizing activity patterns in the feature space.

### 2. Data Preprocessing

The preprocessing stage prepares the data for clustering.

Main steps:

* handling missing values;
* removing or processing outliers;
* scaling numerical features;
* checking duplicated records;
* preparing train and test datasets;
* ensuring reproducibility of the pipeline.

### 3. Feature Engineering

Since sensor data often have a time-series nature, additional features can improve clustering quality.

Possible engineered features:

* statistical features;
* mean and standard deviation;
* minimum and maximum values;
* signal magnitude;
* rolling window statistics;
* differences between measurements;
* aggregated features from IMU sensors;
* heart rate-based features.

### 4. Feature Selection and Analysis

At this stage, the most informative features are analyzed and selected.

Methods used:

* correlation analysis;
* variance analysis;
* feature distribution comparison;
* dimensionality reduction;
* visualization with PCA, t-SNE or UMAP;
* model-based feature evaluation if applicable.

### 5. Model Training

Several clustering models are trained and compared.

Possible models:

* K-Means;
* MiniBatchKMeans;
* Gaussian Mixture Model;
* Agglomerative Clustering;
* DBSCAN;
* Birch.

### 6. Model Evaluation

Since the task is unsupervised, internal clustering metrics and visual analysis are used.

Possible evaluation metrics:

* Silhouette Score;
* Davies-Bouldin Index;
* Calinski-Harabasz Index;
* cluster size distribution;
* visual separation of clusters;
* stability of results.

### 7. Hyperparameter Tuning

For each model, important parameters are selected and tested.

Examples:

* number of clusters;
* initialization strategy;
* covariance type for Gaussian Mixture Model;
* distance thresholds;
* batch size;
* random seed.

### 8. Final Prediction

After comparing models, the best-performing approach is selected.
The final model is used to predict clusters for the test dataset.

The result is saved as a submission file for Kaggle.

---

The notebook includes:

* full solution pipeline;
* model comparison;
* final prediction;
* submission file;
* screenshot of the Kaggle leaderboard result
---

## Results

As a result of the project, a clustering pipeline was developed for grouping human activity data collected from wearable sensors. Several unsupervised learning models were tested and compared. The final model was selected based on clustering quality metrics, stability of cluster distribution, and interpretability of the results.

The obtained clusters can be interpreted as different patterns of user activity based on IMU and heart rate data.

---

## Conclusion

This project demonstrates the use of unsupervised machine learning methods for human activity analysis based on wearable sensor data. The developed approach can be useful for activity recognition, health monitoring, fitness analytics, and intelligent systems that process sensor data from wearable devices.

The work includes the full machine learning workflow: data analysis, preprocessing, feature engineering, model training, comparison, hyperparameter tuning, prediction, and final interpretation.
