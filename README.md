# Data_Assn4

## Requirements

- Jupyter Notebook
- Pandas
- Numpy
- Matplotlib
- Seaborn

## Accomplishments

Learned:

- Data preprocessing
- Discretization methods
- Correlation Matrices
- Principle Component Analysis

## Purpose

To Practice various preprocessing and feature selection/extraction techniques.

## Project requirements

1. [10 points] For this question, you will apply different discretization methods to the “close” column of the stock prices dataset. Include the code.
a) Apply equal width discretization to produce 5 bins. Display the first 5 discretized values by using the head() function
b) Apply equal frequency discretization to produce 5 bins. (Note that the quantiles selected in the lecture slides will produce only 4 bins. Therefore, you need to choose the appropriate quantiles that will produce 5 bins).
2. [30 points] Implement entropy-based discretization (supervised discretization) and apply it to the vehicles dataset. Implement it using recursion. Implementing it non-recursively is acceptable, but I imagine it would be hard. Come up with a threshold to stop splitting the data. Note that you must perform the iscretization separately for each feature (column). Print each feature, its discretized ranges, and the corresponding final entropy. For simplicity, only consider bus and van classes:
vehicles_df = pd.read_csv("vehicles.csv")
vehicles_df = vehicles_df[((vehicles_df["class"] == "van") | (vehicles_df["class"] == "bus"))]
vehicles_df["class"] = vehicles_df["class"].replace(["van"],0)
vehicles_df["class"] = vehicles_df["class"].replace(["bus"],1)
3. [20 points] Compute the Mean Absolute Deviation of features (columns) as well correlation matrix of vehicles dataset. Based on the mean absolute deviation, what are the best features? Also, according to the correlation matrix, choose a few features that can/should be removed.

4. [40 points] Principal Component Analysis (PCA). Please see the sample codes in the slides and on Canvas.
a) Apply PCA to vehicles dataset. You can use PCA from sklearn or calculate PCs from eigenvectors of the covariance matrix as described in the lecture.
b) How many PCs are needed to capture 90% of the variance? What about 99%?
c) Use two PCs and visualize the samples. Use different colors or markers for different classes. Do you see any pattern?
d) Get feature importance using PCs similar to what was presented in the lecture. What are your observations?
5. (bonus) [15 points] Apply appropriate text preprocessing operations on White House tweets (only the text)– See the sample code on Canvas. You can use tweet preprocessor for additional preprocessing functionalities, e.g., removing emojis
