# Iris-DecisionTreeClassifier
This program is using DecisionTree to Classified the Iris datasets from sklearn.


## Load and Check all the data's correlation
As we can see the table and Heatmap below.

**petal length** and **petal width** is very **Positive correlation** with the answer. Thus, we can predict these two variables will be important in this classification.

| | sepal length (cm) | sepal width (cm) | petal length (cm) | petal width (cm) | answer |
|---------|---------| ---------| ---------| ---------| ---------|
| sepal length (cm) | 1.000000 | -0.117570 | 0.871754 | 0.817941 | 0.782561 |
| sepal width (cm) | -0.117570 | 1.000000 | -0.428440 | -0.366126 | -0.426658 |
| petal length (cm) | 0.871754 | -0.428440 | 1.000000 | 0.962865 | 0.949035 |
| petal width (cm) | 0.817941 | -0.366126 | 0.962865 | 1.000000 | 0.956547 |
| answer | 0.782561 | -0.426658 | 0.949035 | 0.956547 | 1.000000 |

![alt text](https://raw.githubusercontent.com/ahoucbvtw/Iris-DecisionTreeClassifier/main/Picture/Heatmap.png "Heatmap")


## Train
First, use sklearn's function **train_test_split** to split train and test data.

Then use DecisionTree to train, to find witch variable is the main factor to classify Iris.

As the picture below, use **petal width (cm)** can easier classified witch Iris is setosa, versicolor and virginica. First step in the picture, it used **petal width (cm) ≤ 0.8** to classify witch is setosa, then used **petal width (cm) ≤ 1.75** to classify witch is versicolor or virginica.

![alt text](https://raw.githubusercontent.com/ahoucbvtw/Iris-DecisionTreeClassifier/main/Picture/DecisionTree.png "DecisionTree")


## Verification & Result
In test data, the accuracy was up to 93.3% by use this decision.

Here is the confusion matrix below.

| | 0(預測) | 1(預測) | 2(預測)|
|---------|---------| ---------| ---------| 
| 0(真正) | 10 | 0 | 0 |
| 1(真正) | 0 | 1 | 0 |
| 2(真正) | 0 | 1 | 3 |
