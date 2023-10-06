# Diabetes Prediction
### By [Gloria Pintado](https://github.com/gloriapintado)

For Better Health is a new organization and is recruiting members. I have been hired by this nonprofit organization that wants to help communities far from cities that need medical support.

## The Problem
What are some of the highest indicator that shows to have more possibilities of being at risk of having prediabetes or diabetes? Based on the highest indicators what can we in order to reduce the risk of having prediabetes or diabetes. Getting a solution will reduce not only the risk of having diabetes but also other health problems such as heart disease, vision loss, and other diseases associated with having diabetes.

## Data Source
- Diabetes Health Indicator Dataset from Kaggle
- It contains 70692 rows and 22 columns (features).
- It is a balanced dataset.
- Our target variable is the diabetes binary. \
  Where :\
    0 is for no diabetes \
    1 is for prediabetes or diabetes

## Modeling
Chosen our **Logistic Regression** as our baseline model. Having 2421 false negatives meaning we have to decrease it, for decreasing false negatives we need to used the recall metric. The recall metric score for our baseline was 0.77

![LR Baseline model CM](https://github.com/gloriapintado/Diabetes_Prediction/blob/main/Images/LR%20Baseline%20model%20CM.png)

Chosing **Decision Trees** another model where our recall was 0.65 ,lower than the Logistic Regression. Having also more false negatives and not reducing it.

![Decision Tree model CM](https://github.com/gloriapintado/Diabetes_Prediction/blob/main/Images/Decision%20Tree%20model%20CM.png)

The Receiver Operating Characteristic (ROC) curve shows how our Logistic Regression baseline model is way better model than the Decision Tree Model.
Having in mind that our recall was better in the Logistic Regression baseline model.
     
![Comparing RUC curve for Basline M and DT](https://github.com/gloriapintado/Diabetes_Prediction/blob/main/Images/Comparing%20RUC%20curve%20for%20Basline%20M%20and%20DT.png)

As we can see Logistic Regression was better than Decision Tree. Our next step will be tuning our hyperparameter in our Logistic Regression Model to see if it can change for better. Not doing the hyperparameter tuning in our decision tree since it did a lot worse.
     
## Tuning Hyperparameters for our Logistic Regression Baseline Model

![Tuning](https://github.com/gloriapintado/Diabetes_Prediction/blob/main/Images/Tunning%20Hyperparameters.png)

Tuning our Baseline model with the Penalties, C's, and Solvers did not have a significant impact in our model's performance.

## Features Importance

![Features Importance](https://github.com/gloriapintado/Diabetes_Prediction/blob/main/Images/Features%20Importance.png)

## Recommendations

- Our top ten features that should be more aware to not be at risk of having prediabetes or diabetes are GenHlth, High BP, BMI, HighChol, Age, DiffWalk, Income, PhysHlth, HeartDiseaseorAttack.
- Promote knowledge about diabetes in promotion and prevention campaigns, providing the information necessary to recognize the disease (education and income).
- Create new strategies to dissolve a sedentary lifestyle and promote new healthy habits (DiffWalk, PhysHealth).
- Do medical campaigns where they carry out checkups, such as taking blood pressure, and laboratory tests to know the cholesterol levels in the blood. Consult with nutritionists to change your diet since each person is different and must follow a special diet and know their body mass index (High BP, BMI, and high cholesterol).
- Mostly aimed at people between the ages of 35 and 40 who are the most prone to having this disease (age).

## Next Steps

- Look for outliers since logistic regression is sensitive to outliers in the dataset
- Try to find a better model that works best with this dataset.
- Try new learning machine models.



