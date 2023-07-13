# PCA and Feature Selection(Dimensionality Reduction)

https://towardsdatascience.com/l1-and-l2-regularization-methods-ce25e7fc831c
# Dimensionality Reduction (Feature Selection)

**Feature Selection** is the process where you automatically or manually select those features which contribute most to your prediction variable or output in which you are interested. Having irrelevant features in your data can decrease the accuracy of the models and make your model learn based on irrelevant features.

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/30a8c2df-ce96-47c5-b1cf-d5cc1ffe93ca)

**Dimensionality reduction** is a technique used in machine learning to reduce the number of input features or variables while preserving the important information contained in the data. It is particularly useful when working with high-dimensional datasets where the number of features is large. The goal of dimensionality reduction is to simplify the data representation by transforming it into a lower-dimensional space. This can lead to **several benefits**, such as:

**1. Reduced computational complexity:** High-dimensional data can be computationally expensive to process and analyze. Dimensionality reduction helps in reducing the computational requirements by working with a smaller set of features.

**2. Elimination of irrelevant features:** Not all features in a dataset contribute equally to the overall information. Removing some features may be redundant or irrelevant, which can improve model performance by focusing on the most important information.

**3. Visualization:** Visualizing high-dimensional data is challenging. Dimensionality reduction techniques can project the data onto a lower-dimensional space, typically 2D or 3D, allowing easier visualization and understanding of the underlying patterns.

# Feature selection techniques

Feature selection techniques can be **classified into three main categories:**

**1. Filter Methods:** Filter methods rank features based on statistical measures or heuristic measures that assess the relevance of each feature independently of the machine learning model. Common statistical measures include **correlation coefficients, chi-square test, information gain, and mutual information**. Filter methods are computationally efficient and can be applied as a preprocessing step before training the model.

**2. Wrapper Methods:** Wrapper methods evaluate feature subsets by training and evaluating a machine learning model on different subsets of features. They use a specific machine learning algorithm to assess the performance of different feature subsets. Wrapper methods are computationally more expensive compared to filter methods, but they can capture feature interactions and provide better feature subsets tailored to the specific learning algorithm. Ex: **RFE (Recursive Feature Elimination)** (Mostly used).

**3. Embedded Methods:** Embedded methods incorporate the feature selection process as part of the model training process. These methods typically use regularization techniques, such as **L1 regularization (Lasso) or L2 regularization (Ridge)**, which impose penalties on the model coefficients. The regularization process encourages the model to automatically select the most relevant features during training.

**Note:** If you are working with a Linear model, for example, Linear Regression or Logistic Regression, then use Embedded Methods. But, if you are working tree-based model, then use either Filter Methods or Wrapper Methods. Filter Methods and Wrapper Methods can be used for Classification purposes.

# Introduction to Linear Algebra (Basics)

**Matrix Addition:**


![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/5af6b542-891d-4775-ac38-e8116d13621b)

**Matrix Multiplication:**


![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/3686b64a-82f2-4618-b057-dfd8eb00082f)

**Transpose Matrix:**


![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/19d4b6a5-d402-464b-a5af-83f2457d7cc6)

**Rank:**

Rank means how many unique columns we are getting; those columns can't be made from any other columns. In this case, we got 2 columns. So, Rank=2.

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/af6c5ea9-7cf3-4133-b258-2ce7e34a2bfa)

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/14782ef3-b299-4cdb-bb73-0428375fb0c4)

**Homogeneous System of Linear Equations:**

A linear equation becomes homogeneous when all becomes equal to 0.
Ex: [ 1 1 3 2] -> A+B+3C+2D = 0.

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/fea58b9b-7bc0-456d-943b-2a000f2a69fb)

# Principal Component Analysis (In-depth PCA)

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/38c1a5ee-a6c5-4c63-88f5-4457d8f439a8)

In PCA, some values are calculated based on all the features through eigenvalue and eigenvector; those values carry the whole information.

In Step 2, we have to subtract the mean value from the actual value. 

In Step 4, suppose, there are 4 features. We have to reduce that to 2 or 1 feature(s). In that case, we will use Dimension Reduction. So, we have to select the value of lambda. We can apply either Gaussian Elimination or Cramer's Rule to find out the eigenvalue(s) and eigenvector(s). 

In Step 5-8, we have to subtract the eigenvector from the actual value. Then, we can get the main principal component(s).

**Example:**

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/0762ac32-d26c-4b6a-bf0f-bbbde379ebc2)

**Explanation:**

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/52454a2c-22f8-4ce1-9959-fe0537be1259)

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/1ef3ee77-0748-42db-b746-6a8b6d716efc)

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/29585506-7e63-496a-b059-6b1e891f8a6c)

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/2ab2d8a5-f67c-4eff-bb26-a9de3533d883)

**Gaussian Elimination:**

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/6e170967-995c-46e8-a196-321f35ba9101)

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/63084814-c2be-4ffc-8a1f-f2f6d542969f)

**Cramer's Rule:**

![image](https://github.com/TITHI-KHAN/PCA-and-Feature-Selection-----Dimensionality-Reduction/assets/65033964/70b55d42-52c5-43ad-ba62-34f457747788)





