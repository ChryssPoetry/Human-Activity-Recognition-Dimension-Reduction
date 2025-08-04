# Human-Activity-Recognition-Dimension-Reduction

Overview
This project tackles the Human Activity Recognition (HAR) problem using data collected from smartphone sensors. With 562 features per observation, the objective is to classify one of six physical activities:

Laying

Sitting

Standing

Walking

Walking Downstairs

Walking Upstairs

Given the high dimensionality, we apply feature selection and Principal Component Analysis (PCA) to reduce noise and improve model performance.

🚀 Project Objectives
📉 Reduce dimensionality using:

Variance Threshold (feature selection)

Principal Component Analysis (PCA)

🧪 Train a classification model using K-Nearest Neighbors (KNN)

📊 Visualize explained variance and the effect of dimension reduction

🎯 Optimize model accuracy with fewer features

🗂️ Dataset
The dataset includes sensor readings from 30 volunteers, aged 19 to 48, performing daily activities while wearing a smartphone around the waist.

📈 562 features (accelerometer, gyroscope, etc.)

🎯 1 target variable: activity (6 classes)

Note: Due to size or licensing, the dataset may not be included in the repo. Please ensure activity.csv is available in your working directory.

⚙️ Tech Stack
Python 3.x

Pandas, NumPy

Scikit-learn

Matplotlib, Seaborn

📌 Key Steps
Data Preprocessing

Load and inspect dataset

Split into train/test sets

Feature Selection

Remove low-variance features using VarianceThreshold

Standardization

Normalize feature distributions using StandardScaler

Dimensionality Reduction

Apply PCA to retain 95% of explained variance

Visualize cumulative variance curve

Classification

Train a KNN classifier (k=6)

Evaluate performance before and after PCA

Optimization

Analyze model accuracy for each PCA dimension k ∈ [1, 200]

Identify the optimal number of components for peak performance

📷 Visual Outputs
📈 Cumulative variance plot

🔍 2D scatter plots of PCA-transformed features (train/test)

🧮 Accuracy vs number of PCA components

✅ Results
Significant dimensionality reduction achieved with minimal accuracy loss

Maximum test accuracy observed at X PCA components (see notebook for details)

Demonstrated effectiveness of PCA in high-dimensional classification tasks

📁 Project Structure
bash
Copy
Edit
├── activity.csv               # Dataset (optional - ensure local availability)
├── human_activity_recognition.ipynb
├── README.md
└── assets/
    └── pca_variance_plot.png
📌 Future Improvements
Add other classifiers (e.g., SVM, Random Forest)

Hyperparameter tuning for k in KNN

Evaluate with t-SNE or UMAP for non-linear dimensionality reduction

Deploy model using Streamlit or Flask

👤 Author
Franklin Nwafor
