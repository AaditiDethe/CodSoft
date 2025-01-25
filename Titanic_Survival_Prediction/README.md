# Titanic Survival Prediction

## Aim:
The aim of this project is to create the model and predict whether a passenger on the titanic survived or not based on given features.

## Dataset:
Dataset is 'train.csv' file. Dataset consists of various features like PassengerId, Sex, Survived, Pclass, Name, Age, Ticket, Fare, Cabin, Embarked, SibSp, Parch.
Target column is Survived

## Libraries used:
1. numpy
2. pandas
3. matplotlib.pyplot
4. seaborn
5. sklearn.model_selection.train_test_split
6. sklearn.linear_model.LogisticRegression
7. sklearn.metrics.accuracy_score

## Data Exploration and Preprocessing:
1. The dataset (.csv file) was loaded using pandas as a DataFrame, and its shape and a glimpse of the first 5 rows were displayed using titanic_data.shape and titanic_data.head().
2. Additional information of the data was display using titanic_data.info().
3. Missing values were checked by using titanic_data.isnull().sum() and handled my method like mean imputaion.
4. Getting some statistical measures about the data and displaying by using titanic_data.describe().
5. The count of passengers who survived and those who did not was visualized using sns.countplot(x='Survived',data = titanic_data).
6. The count of male-female who survived and those who did not was visualized usingsns.countplot(x='Sex',data = titanic_data)
7. The count of survivals was visualized with respect to the gender using sns.countplot(x='Sex', hue="Survived", data=titanic_data).
8. The count of survivals was visualized with respect to the Pclass using sns.countplot(x='Pclass', hue="Survived", data=titanic_data).
9. The survival rate by gender was calculated and displayed using titanic_data['Sex'].value_counts().
10. The 'Sex' column and 'Embarked' column (Categorical Column) were converted to numerical column using titanic_data.replace({'Sex':{'male':0, 'female':1}, 'Embarked':{'S':0, 'C':1,'Q':2}}, inplace=True).
11. Separating features and target and dropping unnessesary columns.

## Model Building / Training:
1. The feature matrix x and target vector y were created using relevant columns from the DataFrame.
2. The dataset was split into training and testing sets using train_test_split from sklearn.model_selection.
3. A logistic regression model was initialized and trained on the training data using LogisticRegression from sklearn.linear_model.

## Model Prediction:
1. Evaluating the model using accuracy score.
2. Accuracy on training data and displaying train data accuracy.
3. Accuracy on test data and displaying test data accuracy.
