# **Customer Clustering Project** *(Electricity Sector)*

Project aimed at creating, testing and evaluating an example of a clustering Machine Learning model, using data from customers who consume electricity from a specific energy supplier. In this project, the focus was on the use of the **KMeans** algorithm, but the **AgglomerativeClustering**, **DBSCAN** - (Density-Based Spatial Clustering of Applications with Noise) and **Gaussian Mixture Model** (GMM).

<br>

## Project phases

1. Exploratory data analysis

   * Verification of the general characteristics of the data;
   * Checking for missing data;
   * Checking for inconsistent data;
   * Attribute engineering.

<br>

2. Data transformation

   * Treatment of null or incorrect data;
   * Deletion of irrelevant data;
   * Separation of training and test data;
   * Normalization and/or Standardization of data.

<br>

3. Creation, Testing and Evaluation of Linear Regression Models

   * Creation of models
     1 - KMeans model;
     2 - AgglomerativeClustering Model;
     3 - DBSCAN Model - (Density-Based Spatial Clustering of Applications with Noise);
     4 - GMM Model - (Gaussian Mixture Model).
   * Model training;
   * Model testing;
   * Evaluation of models.

<br>

## Technologies Used

This project was executed using the Python language in the Jupyter Notebook format. The libraries Pandas (Loading, Cleaning and Data Analysis), Matplotlib (Data visualization and graph generation), Sklearn (Creation, training and evaluation of Machine Learning models), Git (Code versioning) and the chosen IDE were used. it was Visual Studio Code, running on Debian Linux.

**Related links:**

* [Debian Linux](https://www.debian.org/index.pt.html)
* [VSCode](https://code.visualstudio.com/)
* [Python](https://www.python.org/)
* [Jupyter](https://jupyter.org/)
* [NumPy](https://numpy.org/)
* [Pandas](https://pandas.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/#)
* [Sklearn](https://scikit-learn.org/stable/)
* [Git](https://git-scm.com/)

### Required Dependencies and Versions

The software and libraries used in the projects had the following versions:

* Python - Version: 3.11.5
* NumPy - Version: 1.26.4
* Pandas - Version: 2.2.1
* Matplotlib - Version: 3.8.3 (matplotlib-inline: 0.1.6)
* Seaborn - Version: 0.13.2
* Scikit-learn - Version: 1.4.1

**Note:** for more details see the file **"requirements.txt"**

## Problems faced

The code may face problems when running using different versions of languages and libraries. Make sure that the versions listed in the "Required Dependencies and Versions" item are correctly installed.

If there is already a development environment with different versions in use on the machine used, a good alternative would be to create a virtual development environment. If in doubt, follow the documentation link.
[Virtual environments and packages](https://docs.python.org/pt-br/3/tutorial/venv.html)

## Results Obtained and Evaluation Metrics:

#### **Model_v1:**

* **Algorithm:** KMeans
* **Clusters:** 7
* **Metrics:**

  * **silhouette score:** 0.8617262776483926

#### **Model_v1:**

* **Algorithm:** KMeans
* **Clusters:** 7
* **Metrics:**

  * **silhouette score:** 0.8617262776483926

#### **Model_v2:**

* **Algorithm:** KMeans
* **Clusters:** 9
* **Metrics:**

  * **silhouette score:** 0.8087643953544675

#### **Model_v3:**

* **Algorithm:** KMeans
* **Clusters:** 6
* **Metrics:**

  * **silhouette score:** 0.8380044143347933

#### **Model_v4:**

* **Algorithm:** KMeans
* **Clusters:** 5
* **Metrics:**

  * **silhouette score:** 0.7322773427162191

#### **Model_v5:**

* **Algorithm:** KMeans
* **Clusters:** 4
* **Metrics:**

  * **silhouette score:** 0.8578440511109866

#### **Comparison model 1:**

* **Algorithm:** AgglomerativeClustering
* **Clusters:** 7

#### **Comparison model 2:**

* **Algorithm:** DBSCAN
  *Parameters:
  * **eps:** 0.03
  * **min samples:** 20
* **Clusters:** 5
* **Noise:** 435 of 40985

#### **Comparison model 3:**

* **Algorithm:** GaussianMixture
* **Clusters:** 7

## **Results:**

For this data set, the model using the KMenas algorithm with 7 clusters and standardized data was the one that seemed to best abstract the characteristics of the data set. The algorithms used for verification managed to replicate the result reasonably well, with the models using AgglomerativeClustering and DBSCAN being used on the same KMeans data set, with around 40 thousand records, while the GaussianMixture algorithm, as it is an algorithm much less computationally expensive, it was used with the total data set containing a little more than 2 million records.

In this sense, what was observed was that the GaussianMixture model managed to abstract data characteristics to a certain extent similar to those labeled by KMeans. DBSCAN, despite creating slightly similar clusters, among all the hyperparameter adjustments tested, ended up labeling, in its best result, 1.06% of the data as noise, which despite not representing something unacceptable, may make the use of this algorithm unfeasible for certain types of problems with this data set.
