# Diabetes_Prediction
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
     
![Comparing RUC curve for Basline M and DT](http://localhost:8888/edit/Images/Comparing%20RUC%20curve%20for%20Basline%20M%20and%20DT.png)
     
