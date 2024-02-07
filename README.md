# classificationTask_ML

## Summary of the project:

### Overview of data:
 The dataset I chose for the signature term project is centered around the estimation of obesity levels in individuals from Mexico, Peru, and Colombia. It includes data from people aged between 14 and 61, encompassing various eating habits and physical conditions. It contains 2111 records and 17 attributes, offering a comprehensive view of factors influencing obesity. Data does not contain any missing values. The dataset was obtained from Kaggle.
The prediction variable here was 'NObeyesdad' which contains 7 levels of weight. These levels are:

Insufficient Weight
Normal Weight
Overweight Level I
Overweight Level II
Obesity Type I
Obesity Type II
Obesity Type III

The features used here for my models out of the 17 columns are all but two - SMOKE (Whether individual smokes or not, sometimes or always) and SCC (Whether individuals kept calorie consumption monitoring). The list of features used were:
Age
Height
Weight
FCVC - Frequency of consumption of vegetables
NCP - Number of main meals
CH2O - Consumption of water daily
FAF - Physical activity frequency
TUE - Time using technology devices
Gender
family_history_with_overweight
FAVC - Frequent consumption of high caloric food
CAEC - Consumption of food between meals
CALC - Consumption of alcohol
MTRANS - Transportation used

Along with this, data shaping had to be done. The main point here was that the dataset did not contain missing values, therefore missing values were randomly generated in the dataset in different columns. Feature engineering had to be performed where a new column 'BMI' was introduced. This column is the Body Mass Index column, which was calculated as : weight/(height)^2.


Algorithms chosen:
Naive Bayes - As a classifier, fast, handles high-dimensionality data
Support Vector Machines - Handles non-linear classification
Decision Tree - Efficiency and generalization
Naive Bayes:

Fast: Naive Bayes relies on Bayes' theorem and simple conditional probability calculations. These calculations are computationally efficient, making Naive Bayes a fast algorithm for training and prediction. This is especially beneficial when dealing with large datasets.
Handles high-dimensionality data: Naive Bayes assumes independence between features, which simplifies the calculation of conditional probabilities. This allows it to handle high-dimensional data effectively without suffering from the curse of dimensionality, where the number of parameters to estimate grows exponentially with the number of features.
Support Vector Machines (SVM):

Handles non-linear classification: SVMs can map the data to a higher-dimensional space using kernel functions, allowing them to model complex relationships between features. This makes them well-suited for non-linear classification problems where decision boundaries cannot be easily represented by linear functions.
Decision Tree:

Efficiency: Decision trees are relatively simple and efficient to train. They use a greedy splitting algorithm that sequentially splits the data into smaller and purer subsets based on the most informative features. This makes them ideal for real-time applications and resource-constrained environments.
Generalization: By choosing features that maximize information gain, decision trees can learn robust models that generalize well to unseen data. This helps them avoid overfitting and perform well on test data.

The algorithms performed very well based on model evaluation criteria such as confusion matrices and other metrics Precision, Recall and F1 scores.
The decision tree model especially proved to be very successful where we obtained an accuracy score of more than 96%. The model did not seem to be overfitting as well, as other metrics like utilizing k-fold cross-validation techniques showed that the model still performed very well. This was important as k-fold introduces random subsets of the data to check the model on.

The training and validation subsets of the data was chosen in a 70:30 split and copies of the downloaded dataset was used in different ways depending on the data encoding requirements of the models.

Issues that needed more attention:
Understanding that accuracies, scores describing metrics are not the only determining factors in the fit of the model and how well it performs. I realized and learnt throughout the process how there are various other parameters that could be tweaked.
