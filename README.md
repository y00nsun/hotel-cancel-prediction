# 🏨 Predicting Hotel Booking Cancellations
### Objective
- The objective of this project is to develop a model that can accurately predict whether a customer will cancel their hotel booking. 
- By identifying patterns and factors that influence cancellations, the model aims to help hotel management mitigate revenue losses and improve customer retention strategies.
<br>

## 1. Data Exploration
### (1) Checking for Missing/Outliers
- Checked for missing values for each feature in the ‘train’ dataset. No missing values found.
- Plotted a boxplot for the numerical feature 'avg_price_per_room' to check for outliers.

### (2) Checking Data Distribution
- Used the `describe()` method to check the mean, standard deviation, quartiles, minimum, and maximum for each feature.
- Used the `hist()` method to plot histograms for all features and visually confirm the data distribution.

### (3) Checking Relationships Between Attributes
- Investigated the relationships between different attributes using scatter plots and correlation matrices (not detailed here but part of the analysis process).

### (4) Processing Categorical Attributes
- Applied one-hot encoding to categorical attributes to create boolean features for each categorical value. Used the `get_dummies()` method from the Pandas library.

## 2. Selection Process for Attributes Used in the Model
- Excluded the target value ‘booking_status’ and the ‘Booking_ID’ feature, which has no impact on the prediction outcome, from the input data (X). Additional features were included or excluded based on subsequent test results.

## 3. Model Selection Process
### (1) Decision Tree
- A Decision Tree provides intuitive interpretations and identifies major variables and splitting criteria compared to other classification techniques such as Logistic Regression. Despite the high possibility of overfitting, this can be resolved by pruning using parameters like max_depth.

### (2) Model Hyperparameter Selection Process and Rationale
- **max_depth:** If the maximum height of the tree is not specified, it will continue to classify until the leaf nodes are pure, causing overfitting. Therefore, this parameter is essential for appropriate pruning. The optimal number was specified to avoid overfitting during execution.
- **min_samples_split:** Specifies the minimum number of samples required to split an internal node. A higher value leads to more pruning, so it was adjusted to prevent overfitting.


## 4. Result
|   Model Type  |  Accuracy  |
|:-------------:|:----------:|
| Decision Tree |  86.__%    |  

<br>

Final Evaluation Date : 2023-06-23
