# Prediction of Product Sales
## Sales prediction for food items sold at various stores

**Author**: Carla Cloete

### Business problem:

A retailer would like to understand the properties of products and outlets that play crucial roles in increasing sales.


### Data:

Outlet Sales Data: https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view?usp=sharing

For this dataset, there were 8523 rows and 12 columns

**Data Dictionary**

<img width="342" alt="Sales Prediction Data Dictionary" src="https://github.com/Carla9711/Prediction-of-Product-Sales/assets/138701194/bd530738-c9e2-41ff-8740-12d7ebb0fd61">


## Methods
- The following steps were taken to clean the dataset:
  -  Duplicate values were evaluated 
  -  Inconsistent categorical values were evaluated and replaced
  -  Impossible numerical values were evaluated
    
- Next, each feature was explored:
  - Boxplots and histograms were ploted for numerical data
    
    <img width="429" alt="Exploratory_Numeric_Item_Visability" src="https://github.com/Carla9711/Prediction-of-Product-Sales/assets/138701194/9b304554-d663-46e2-bf14-e60cad6b9010">

As can be seen from the graph above Item_Visability is skewed to the right and most products have low visability in stores.

  - Countplots were plotted for categorical data

<img width="406" alt="Exploratory_Categorical_Item_Fat_Content" src="https://github.com/Carla9711/Prediction-of-Product-Sales/assets/138701194/29dfdbb7-c4f4-4c49-bf29-474169698214">

As can be seen from the graph above, most items have a low fat content.

- After the exploratory analysis, an explanatory analysis was done on each feature in relation to the target:
  - For numerical features a regression plot was plotted

     <img width="365" alt="Explanatory_Numeric_Item_MRP" src="https://github.com/Carla9711/Prediction-of-Product-Sales/assets/138701194/08dd5a40-c44c-44b5-bd05-547e1e37f48b">

As can be seen from the figure above, Item_MRP is positively correlated to Item_Outlet_Sales
  - For categorical features bar plots and strip plots were plotted
    
<img width="391" alt="Explanatory_Categorical_Item_Fat_Content" src="https://github.com/Carla9711/Prediction-of-Product-Sales/assets/138701194/4b78671a-63b4-424a-bfe0-9180930986a9">

As can be seen from the graph above, Low Fat and Regular Fat products have similar average sales and a similar distribution of sales.
  
- Each feature was assessed in terms of cardinality, the business case and the relation to the target. The following features were dropped from the dataset
  - Outlet_Identifier is not a property of the outlet and was therefore dropped.
  - Item_Type had a high cardinality of 16 and each item type had a similar distribution of sales and was therefore dropped.
 
- The following steps were taken to prepare the data for modeling
  - Numerical Columns
    - Missing values were imputed with the median
    - Columns were scaled   
  - Ordinal
    - Missing values were imputed with a constant
    - Columns were ordinal encoded and scaled
  - Nominal
    - Columns were hot one encoded        

## Results
- Four models were fitted and evaluated:
  - Baseline Model
  - Linear Regression
  - Random Forest
  - Random Forest Tuned

The final results of each model is displayed below

<img width="346" alt="Model Results" src="https://github.com/Carla9711/Prediction-of-Product-Sales/assets/138701194/1e83c1d8-aea6-4877-a7d2-096482bb1410">

## Model

The recommened model is the tuned Random Forest model as it provided the best evaluation scores.

The R squared value for this model is 0.6 which is above 0.5 and is acceptable but not ideal. A R squared value closer to 1 would be more favourable.

Furthermore, the MAE for the model indicates that the predicted target can be expected to be about 734.6 units away from the actual target. This is about 34% of the average target price.

## Recommendations:

To achive higher R squared values and lower MAE, MSE and RSME values the dataset should be evaluated again. Columns that have little affect on the target should be dropped and new features that have better correlations to the target should be sourced.

## Limitations & Next Steps

The analysis and modeling was limited to the dataset provided. Next step would be to consult the retailer to see if there's additional data points (i.e. features) that can be used for modeling.


### For further information


For any additional questions, please contact CLTCAR010@myuct.ac.za

