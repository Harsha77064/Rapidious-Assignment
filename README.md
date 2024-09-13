The provided code demonstrates the application of various machine learning algorithms to the Epicurious Recipes (Epirecipes) dataset, with the goal of predicting whether a recipe is classified as a dessert. The workflow includes several models, such as Logistic Regression, Gaussian Naive Bayes, K-Nearest Neighbors (KNN), Random Forest, Support Vector Machine (SVM), Decision Trees, AdaBoost, and a Neural Network implemented using TensorFlow/Keras.

Data Preprocessing:
The dataset epi_r.csv is loaded and filtered to exclude recipes with extremely high calorie counts.
The target variable is the "dessert" label, and features like calories, protein, fat, and sodium are used for model input.
Machine Learning Models:
Logistic Regression:

This classifier is used to predict whether a recipe is a dessert. The model performs with high accuracy (96%), demonstrating strong precision and recall.
The model’s performance is visualized using an ROC curve.
Gaussian Naive Bayes:

Gaussian Naive Bayes is another model tested, achieving 94% accuracy on the test data, slightly lower than Logistic Regression.
K-Nearest Neighbors (KNN):

KNN is applied and optimized using GridSearchCV to determine the best number of neighbors, with 4 being optimal. The final accuracy is 78.7%.
Random Forest:

A Random Forest classifier is implemented, and hyperparameter tuning is performed using GridSearchCV. After tuning, the model achieves an accuracy of 82%.
Support Vector Machine (SVM):

The SVM model with a linear kernel achieves an accuracy of 94%, which matches the performance of Logistic Regression.
Decision Tree:

A Decision Tree model is trained, and the tree structure is visualized using plot_tree to show the decision-making process of the model.
AdaBoost:

AdaBoost, a boosting ensemble technique, is applied with 50 estimators, resulting in an accuracy of 93.3%.

Neural Network (TensorFlow/Keras):
A feedforward neural network is built using Keras:
The model consists of two hidden layers, the first with 64 neurons and the second with 32 neurons, both using ReLU activation.
The output layer uses a sigmoid activation function for binary classification.
The model is trained for 10 epochs using the Adam optimizer and binary crossentropy loss.
After training, the neural network achieves a 94% accuracy on the test data, comparable to the Logistic Regression and SVM models.
Clustering:
K-Means clustering is applied to group recipes based on calorie and protein content, although detailed clustering results or visualizations were not provided in this code snippet.
This workflow showcases how different machine learning models can be used for classification tasks and how they can be optimized for performance on a dataset.


**Visualisation**
Dataset Overview:

The dataset contains 20,052 rows and 680 columns, with columns representing different food recipes and various attributes like ratings, calories, protein, fat, and sodium.
Handling Missing and Abnormal Values:

Calories: Rows where calories exceeded 10,000 were removed, considering them outliers. Missing values in the calorie column were filled with the mean value (487.9).
Duplicates: Duplicate rows were identified and removed. After removing duplicates, the dataset contained 17,719 rows.
Exploratory Data Analysis (EDA):

Distribution of Ratings: A histogram and boxplot showed the distribution of recipe ratings, with the most frequent rating being around 4.375.
Calories Distribution: A violin plot, boxplot, and histogram visualized the spread of calories across different recipes.
Scatter Plot: A scatter plot between calories and ratings indicated no clear linear relationship.
Column Manipulation:

Unnecessary columns like title and calories were dropped as part of data cleaning.
The final dataset consisted of the columns rating, protein, fat, and sodium.
Visualizations:

Several plots like histograms, scatter plots, and joint plots were used to visualize the relationships between the numerical features such as rating, calories, protein, etc.
Key Statistics:

Rating: Mean rating is around 3.72, with a standard deviation of 1.32.
Calories: The calories had a mean of 502, ranging from 0 to 9831.
Protein: Mean protein is 22.36g, with significant outliers.
Sodium: Some recipes had extremely high sodium values, with a max value of 132,220.
The analysis focused on cleaning the dataset, handling missing values, identifying patterns in the distribution of ratings, calories, and other features, and visualizing those relationships.






