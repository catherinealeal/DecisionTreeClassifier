# Decision Tree Classifier to Predict Home Type 

## Goal 

- Predict the 'Type' of home using a decision tree.
- The stopping condition is the depth of the tree.
- The impurity measure is either entropy or gini.

## Create a Decision Tree 
- Using scikit-learn to create a multi class classifer for the data set using the Entropy impurity measure and a max depth of 3.
- The algorithm can only handle categorical data, so that needs to be preprocessed using an one hot encoding.

![image](https://github.com/catherinealeal/DecisionTreeClassifier/assets/100166102/3a5db247-f022-4e36-bcb5-f402c12f6411)

The type of building is most correlated to the landsize, year built, and building area. These are the attributes on which the tree was built, using them as the splitting conditions for child nodes.

## Calculate the Accuracy and Display Learning Curve
- Using the scikit-learn library to create many decision trees, each one with a different configuration (aka hyperparameters)
- Creating 28 different trees by:
   - Varying the max depth from 2 to 15 with the Gini Index as the impurity measure
   - Varying the max depth from 2 to 15 with the Entropy as the impurity measure
- For each of the 28 decistion trees, calculat the error rate by using the data in the training set and test set.

![image](https://github.com/catherinealeal/DecisionTreeClassifier/assets/100166102/f54da2f8-8d37-4e0b-b0a5-253d65e1af06)

## Conclusion 
- From this plot, it can be seen that the error rates of the training data (regardless of the impurity measure) have signifigantly lower error rates as compared to the testing data error rates as max depth increases. This trend makes sense because a tree trained on a certain dataset should work better on that specific dataset then it would on a new dataset on which it was not trained.
- Looking at the difference between the test data errors for the gini and entropy measures, it can be seen that the trees using entropy as the impurity measure have lower errors rates than trees using gini.

## View full project [here](https://github.com/catherinealeal/DecisionTreeClassifier/blob/main/DecisionTreeClassifier.ipynb)
