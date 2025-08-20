# AI-Powered Motion Clustering System

### Project Introduction

This project is an AI-driven system designed to analyze and cluster complex physical motions. Specifically, it applies machine learning techniques to classify the trajectories of objects falling freely through a fluid. The project combines **physics-based feature extraction** from videos with deep learning models to uncover hidden patterns within the data.

### Key Objectives

* **Physical Feature Extraction:** Use **OpenCV** to process videos and extract essential physical parameters such as velocity, coordinates, and oscillation frequency.
* **Intelligent Clustering:** Apply an **Autoencoder** model for dimensionality reduction and **KMeans** to automatically group similar motions into distinct clusters (e.g., steady, zigzag, spiral trajectories).
* **Bridging Physics and AI:** Connect empirical data with machine learning models to provide new insights into fluid mechanics.

### Processing Pipeline

The project follows a clear, step-by-step workflow:

1.  **Video Preprocessing & Feature Extraction:**
    * **OpenCV** is used to identify and track the object frame by frame.
    * The trajectory is extracted, and physical quantities like speed and oscillation frequency are calculated.
    * These features are then stored in a data frame for further processing.

2.  **Data Preprocessing:**
    * A **PowerTransformer** from `scikit-learn` is used to normalize the data, ensuring all features are on a comparable scale.

3.  **Deep Learning (Autoencoder):**
    * An **Autoencoder** is built with **PyTorch** to compress the feature data into a low-dimensional latent space.
    * The goal is to find a compact representation that preserves the essential information of the data.

4.  **Clustering (KMeans):**
    * The **KMeans** algorithm is applied to the latent space to perform clustering.
    * The resulting clusters correspond to different types of motion.

5.  **Visualization & Evaluation:**
    * **PCA** is used to reduce the latent space to 2D for easy plotting.
    * A scatter plot visualizes the motion clusters.
    * The clustering quality is evaluated using the **Silhouette Score**. 

### Technologies & Libraries

* **Language:** Python
* **Video Processing:** OpenCV
* **Deep Learning:** PyTorch
* **Machine Learning:** Scikit-learn
* **Data Science:** Pandas, Numpy
* **Visualization:** Matplotlib, Seaborn

### 📈 Results

The system successfully classified motion trajectories and produced distinct clusters, helping differentiate between various motion regimes like `Steady`, `Periodic (Zigzag)`, and `Chaotic`. The results demonstrate the ability of machine learning algorithms to provide new insights into classical mechanics problems.

### Future Directions

* **Expanded Feature Set:** Incorporate more complex physical features like the Reynolds number (Re) and moment of inertia.
* **Time-Series Modeling:** Extend the project to time-series deep learning models like **LSTMs** to directly classify entire trajectory sequences.
* **Deployment:** Develop a user interface for easy video uploads and cluster analysis.

***

This video shows how to create an engaging README for a data science project on GitHub. [How to Create an Engaging README for your Data Science Project on GitHub](https://www.youtube.com/watch?v=5UhBnXWbCMY)
http://googleusercontent.com/youtube_content/0

