# Predicting King County House Prices with Multiple Linear Regression

> Image

# Project Overview 
The aim of this project is to develop a Multiple Linear Regression Model to accurately predict the sale prices of houses in King County. Through careful data analysis and exploratory data analysis techniques, we will preprocess and clean the dataset to create a data frame for regression modeling. By analyzing key features such as square footage, number of bedrooms, location(waterfront or not), and more, we aim to uncover valuable insights that influence house prices.

# Business Understanding
Business understanding is essential for a real estate agency to effectively serve its clients. It serves as the foundation for successful operations and sustainable growth in the real estate industry. You need to understand the listing prices and how it affects buyers and sellers in making informed decisions. Identifying the expectations, preferences, and needs of the clients, and knowing what the clients want from the agency’s services, especially in terms of property evaluation is crucial.  Factors considered in the evaluation are:
* I.	Size and layout, the size of the property, the number of bedrooms and bathrooms, and the layout are crucial.
* II.	Condition, the property’s condition, including any need for repairs or renovations, can affect its value.
* III.	Location: The property location influences its value, factors like proximity to schools, parks, shopping malls, and transportation can impact the value
Gaining insight into the local housing market dynamics in the dataset such as the fluctuations in supply and demand, seasonality, and regional variations in property value is important.

# Main objective
* To develop a Multiple Linear Regression Model to accurately predict the sale prices of houses in King County
  
# Specific objective 
* Which features are identified as relevant for the Multiple Linear Regression Model, considering factors like size, layout, condition, and location?
* How do house prices vary concerning different features, such as square footage, the number of bedrooms, and location?
* How is the initial Multiple Linear Regression Model developed as a baseline?
* What is the outcome of the Exploratory Data Analysis in terms of understanding the distribution of key variables and relationships?
  

# Data understanding
The King County House Sales project dataset is stored in a file named kc_house_data.csv, accompanied by column descriptions available in column_names.md. It contains information relevant to house sales in King County, providing a comprehensive set of features. 

1. ## Price Distribution

> Image

2. ## Vitualizing categorical data

> Image of conditions with high correlation in relation to price.

3. ## Multicollinearity

Considering the presence of multicollinearity between 'sqft_above' and 'sqft_living', and recognizing that 'sqft_living' exhibits the highest correlation with our target variable, we have decided to drop the 'sqft_above' feature to mitigate the effects of multicollinearity in our analysis." 

> Heat map image.

### Modelling.

#### Multiple linear regression with features strongly correlating price

Multiple linear regression incorporating the top four variables showing the strongest correlations with price

> Image

#### Multiple linear regression with features strongly correlating price without multicollinearity

> Image

4. ## Residuals Normality Assumption

In this step, we use a QQ-plot to verify if the residuals in the multiple linear regression model adhere to a normal distribution. This is essential for ensuring the validity of regression analysis.

> Image

5. ## Training model with random forest

Random Forest - Mean Squared Error Train: 0.01
Random Forest - Mean Squared Error Test: 0.08
Random Forest - R-Squared Train: 0.96
Random Forest - R-Squared Test: 0.71

# Recommendation and Conclusions
## Recommendation.

A larger dataset is needed for a thorough analysis of these unique qualities.

## Conclusions
The dataset contains information about house prices, with a diverse range of prices from $78,000 to $7,700,000. The mean and median prices are close, suggesting a roughly symmetric distribution, but with considerable variability due to some extremely high-priced houses.

The analysis of the "grade" and "condition" features provides insights into the quality and condition of houses in the dataset. Most houses fall within the average quality and condition categories. It is essential to consider the condition of the house as it can significantly impact its price and other characteristics

Bivariate analysis shows that houses with a waterfront view tend to have a wider price distribution, with higher upper quartile prices, compared to houses without a waterfront view.

The multivariate analysis using linear regression models reveals that features like grade, bathrooms, and square footage of living space (sqft_living) have a significant impact on the price of a house. Model 2, which includes these features, performs better in terms of R-squared and is free from multicollinearity issues.
The residuals of Model 2 appear to follow a normal distribution, which is essential for the validity of linear regression analysis.

Two models were trained: a linear regression model and a random forest model. The linear regression model achieved good results with low Mean Squared Error and high R-squared values, indicating its strong predictive performance. The random forest model performed even better on the training set

Feature selection was done based on correlations with the target variable (price), and multicollinearity was addressed by removing one of the correlated features. The analysis and modeling suggest that the price of a house can be predicted effectively using features such as grade, bathrooms, and square footage of living space. The linear regression model provides a good baseline for prediction, while more complex models like random forest may be used for even better results
