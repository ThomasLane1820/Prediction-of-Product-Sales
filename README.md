# Prediction-of-Product-Sales
Author: Thomas Lane

## Project Overview

- The overarching goal of this project is to accurately predict product sales and ultimately increase revenue for a potential stakeholder.
-  The first step was to clean the dirty data set.
-  Next I had to visualize and display all relevant information about each feature.
-  I then had to clean the data for the purposes of implementing machine learning.
-  Using and optimizing various regression models to make product sales with the lowest error.

  

## Data visualization
![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/f5a2c2f9-36f1-4405-b1e4-e5dea92ddd81)
- This histogram shows that there are over 1,500 items that generate less than $500 in sales.
- We can potentially take a closer look into these items to see why that may be the case.





![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/d51e6016-8d6e-4d65-843f-00cba7bb85c7)
- Knowing how well seafood performs overall, we might want to look into upping the seafood inventory at certain locations.
- I would also reccommend upping the Starchy food inventory due to it's consistentcy.
- The top three item groups are all performing very well.



![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/1a1b0f20-56e0-470b-a53a-147ef23c55d9)

![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/e9b8c45d-c840-482d-9641-cf4aa44f552d)
- Visualizing the correlation found between "Item_MRP" and "Item_Outlet_Sales" appears to show that the higher the price of an item the higher the item's potential sales.
- We might be able to leverage this by adding more high quality, high price items to our stock.

### Analyzing Coefficients and importaant features
![Scuffed_coefficients](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/108cd507-0d65-4fb5-bd1b-698ec17e0254)
- Although the data isn't quite calibrated properly, the three most impactful features are:
  - Outlet_Identifier_OUT013
  - Outlet_Type_Supermarket Type 1
  - Outlet_Location_Type_Tier 3
 
![Important_Features](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/fd70117a-9691-4f13-a625-e90026162f42)
- The five most important features are:
  - Item_MRP
  - Item_Visibility
  - Outlet_Type_Supermarket Type 1
  - Outlet_Type_Supermarket Type3
  - Item_weight
- It is clear and understandable that the top 4 most important features are Item cost, Item visibility, and the outlet type.
- I believe the most important piece of information here is related to the outlet sizes that perform best.
  
## Evaluation Results
![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/336a7666-eb6a-48c5-843b-f3e5cbc7252b)
- After creating multiple models, the model with the highest R^2 was the Optimized Random Tree Model.
- This model also had the lowest MAE and RMSE, making it the model with the least error.
- Now the model is still off by about 40% so there is still plenty of room for improvement.
  
## Next Steps
- While I have cleaned and optimized a model far beyond default hyperparameters ther is still much that can be done.
  -  There is still further data cleaning opportunities such as:
      - Editing the Item_Identifier Collumn to remove the numbers.
      - Creating a third Item_Fat_Content option for non-consumable items.
  - There are more advanced models I can use to predict sales with.
  - Making the notebook neater as a whole.
