# Predicting Prices Of Homes Using Multiple Linear Regression
## Making Recommendations For Home Sellers

**Authors**: Vivienne DiFrancesco

The contents of this repository detail an ordinary least squares (OLS) linear regression model to predict housing sell prices in King County Washington. This analysis is detailed in hopes of making the work accessible and replicable.


## Business problem

The purpose of this project was to make a linear regression model to predict the sell prices of homes for home owners. Using the model built, people in King County who are looking to sell their homes can gain insights. The predictions could be helpful for homeowners to get a better price when selling their home or to know what price to expect when selling their home.


## Data
The data used for this project was records of houses sold in King County Washington, which includes the urban center of Seattle. The data can be found in this repo as a csv and the file is called "kc_house_data" The dataset contained over 21,000 records and included homes priced between $7.7 million  and $78,000. The houses were sold between 5/2/2014 and 5/27/2015. The data includes information about squarefootage of the homes, condition, floors, year built, renovations, bedrooms, bathrooms, and size of the lot. 


## Methods
- The OSEMiN data science workflow was used through this project.
- The data was first analyzed for each of the independent variables to identify which were appropriate to be considered as categories. Factors such as zipcode were used as categorical features in the model. Other variables that did not meet assumptions for normality or linearity were dropped. Some variables were also dropped since they were too full of zero values to be meaningful. 
- The statsmodels OLS linear regression was used for modeling. For each model iteration a train-test-split and cross validation was done to assess model quality. A new model iteration was done after each change to note how the model improved or declined due to the change.
- First, outliers were removed using the interquartile range (IQR) method, then multicolinearity and variance inflation factor (VIF) were addressed, then the dependent variable (prices) were log transformed to better meet assumptions of normality, residual homoscedasticity, and residual normality. 
- Features with insignificant p-values were removed except in the case of categorical data. For categorical features, if a majority of the categories were significant, then the whole category remained in the model. 

## Results


#### Home Prices By Location
![visual1](https://raw.githubusercontent.com/AnyOldRandomNameWillDOo/Module-2-Final-Project/master/Visuals/Home%20Prices%20By%20Location.png)
> Prices of the homes in the dataset by location.

#### Home Price By Squarefoot Living Space
![visual2](https://raw.githubusercontent.com/AnyOldRandomNameWillDOo/Module-2-Final-Project/master/Visuals/Home%20Price%20By%20Squarefoot%20Living%20Space.png)
> Increasing squarefoot living space increases the home price.

#### Average Home Price By Number Of Bathrooms
![visual3](https://raw.githubusercontent.com/AnyOldRandomNameWillDOo/Module-2-Final-Project/master/Visuals/Average%20Home%20Price%20By%20Number%20Of%20Bathrooms.png)
> Increasing bathrooms increases the home price.

#### Average Home Price By Grade
![visual4](https://raw.githubusercontent.com/AnyOldRandomNameWillDOo/Module-2-Final-Project/master/Visuals/Average%20Home%20Price%20By%20Grade.png)
> Increasing the grade from the county assessor increases the home price.

#### Average Home Price By Condition
![visual5](https://raw.githubusercontent.com/AnyOldRandomNameWillDOo/Module-2-Final-Project/master/Visuals/Average%20Home%20Price%20By%20Condition.png)
> Increasing the condition from the county assessor increases the home price.

## Recommendations:

- Adding bathrooms to your home will add value.
- Adding square feet to the living space of your home will add value.
- Increasing grade and condition ratings of your home will add value.

Ultimately, home sellers will find more value in their homes by focusing on meaningful renovations. Adding square feet, and bathrooms are value adding renovations where adding new floors or basements will not be very value adding. Increasing condition and grade will increase the sell price. The condition and grade are based largely on quality building materials and doing home repairs.


## Further Directions

- Stepwise feature selection - If I were to keep working with this data set I would try taking the perspective of doing a step wise feature selection. It would be interesting to see if such an approach from the beginning would improve model quality and/or residuals.

- Scaling the data - If I were to keep working, I could try another iteration of the model where I scaled features. I briefly dabbled with transforming feature values to z-scores and it did seem to improve residual normality but greatly reduced the R squared. It would be an interesting experiment to try different methods of scaling or transforming the data to see what worked best and how the model changed.


## For further information
Please review the narrative of the analysis in [the main notebook](./main_notebook.ipynb) or review the [presentation slides](./HousingRecommendationsSlides.pdf)



## Repository Structure:

- README.md: The top level README for reviewers of this project
- main_notebook.ipynb: narritive documentation of analysis in jupyter notebook
- HousingRecommendationsSlides.pdf: pdf version of project presentation slides
- Visuals folder: Contains main visuals for the project
- Data folder: Contains datasets used in this project
- Scratch Notebook folder: contains jupyter notebook of work done on this presentation in an unpolished format

