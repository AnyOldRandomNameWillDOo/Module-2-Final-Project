# Predicting Prices Of Homes Using Multiple Linear Regression
## Making Recommendations For Home Sellers

**Authors**: Vivienne DiFrancesco

The contents of this repository detail an ordinary least squares (OLS) linear regression model to predict housing sell prices in King County Washington. This analysis is detailed in hopes of making the work accessible and replicable.


## Business problem

The purpose of this project was to make a linear regression model to predict the sell prices of homes. Using the model built, people in King County who are looking to sell their homes can gain insights. The predictions could be helpful for homeowners to get a better price when selling their home or to know what price to expect when selling their home.


## Data
The data used for this project was records of houses sold in King County Washington, which includes the urban center of Seattle. The data can be found in this repo as a csv and the file is called "kc_house_data" The dataset contained over 21,000 records and included homes priced between $7.7 million  and $78,000. The houses were sold between 5/2/2014 and 5/27/2015. The data includes information about squarefootage of the homes, condition, floors, year built, renovations, bedrooms, bathrooms, and size of the lot. 


## Methods
- The OSEMiN data science workflow was used through this project.
- The data was first analyzed for each of the independent variables to identify which were appropriate to be considered as categories. Factors such as zipcode were used as categorical features in the model. Other variables that did not meet assumptions for normality or linearity were dropped. Some variables were also dropped since they were too full of zero values to be meaningful. 
- The statsmodels OLS linear regression was used for modeling. For each model iteration a train-test-split and cross validation was done to assess model quality. A new model iteration was done after each change to note how the model improved or declined due to the change.
- First, outliers were removed using the interquartile range (IQR) method, then multicolinearity and variance inflation factor (VIF) were addressed, then the dependent variable (prices) were log transformed to better meet assumptions of normality, residual homoscedasticity, and residual normality. 
- Features with insignificant p-values were removed except in the case of categorical data. For categorical features, if a majority of the categories were significant, then the whole category remained in the model. 

## Results

### Here are examples of how to embed images from your sub-folder


#### Visual 1
![graph1](https://github.com/AnyOldRandomNameWillDOo/Module-2-Final-Project/blob/master/Home%20Prices%20By%20Location.png)
> Location makes a big difference on home prices but can not be controlled by owners.

#### Visual 2
![graph2](./images/visual2.png)
> Sentence about visualization.


## Recommendations:

More of your own text here


## Limitations & Next Steps

More of your own text here


### For further information
Please review the narrative of our analysis in [our jupyter notebook](./main_notebook.ipynb) or review our [presentation](./SampleProjectSlides.pdf)

For any additional questions, please contact **email, email, email)


##### Repository Structure:

Here is where you would describe the structure of your repoistory and its contents, for example:

```

├── README.md                       <- The top-level README for reviewers of this project.
├── main_notebook.ipynb             <- narrative documentation of analysis in jupyter notebook
├── presentation.pdf                <- pdf version of project presentation
└── images
    └── images                          <- both sourced externally and generated from code

```
