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
 
Outlet_Identifier is not a property of the outlet and therefore will be dropped. Item_Type has a high cardinality of 16 and have little effect on the target (Item_Outlet_Sales) and therefore will also be dropped.
- The following steps were taken to prepare the data for modeling
  - Numerical
  - Categorical
  - Nominal
- The          

## Results

### Here are examples of how to embed images from your sub-folder


#### Visual 1 Title
![sample image](project1_sample_image.png)

> Sentence about visualization.

#### Visual 2 Title

## Model

Describe your final model

Report the most important metrics

Refer to the metrics to describe how well the model would solve the business problem

## Recommendations:

More of your own text here


## Limitations & Next Steps

More of your own text here


### For further information


For any additional questions, please contact **email**
