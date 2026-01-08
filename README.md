# Prediction of Product Sales
Author: Thomas Lane

## Project Overview

- The overarching goal of this project is to accurately predict product sales and ultimately increase revenue for a potential stakeholder.
-  The first step was to clean the dirty data set.
-  Next I had to visualize and display all relevant information about each feature.
-  I then had to clean the data for the purposes of implementing machine learning.
-  Using and optimizing various regression models to make product sales with the lowest error.

  

## Data visualization
![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/f5a2c2f9-36f1-4405-b1e4-e5dea92ddd81)
- The histogram shows that there are over 1,500 items that generate less than $500 in sales.
- We can take a closer look into these items to see if there's anything we can do to improve sales.
  - We could improve Item_Visibility to improve sales.
      - If visibility isn't an issue the item's location in the store could be another potential symptom of low sales.
  - Look into which stores sell the the poorly performing items, and compare the item's sales to the overall performance of the indivicual store.
      - Doing this could put more accountability onto the store itself rather than the item.
  


![Screenshot 2024-01-17 141600](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/f7f97b87-e1bc-4141-be31-4cc0674c49b5)
- Based off the boxplot seafood and starchy foods are the two most consistent sellers.
  - Seafood has the highest median value and ties starchy foods for highest 75th percentile.
  - Starchy foods have the highest minimum value, and are tied for highest 75th percentile.
- taking a closer look into "others", "baking foods", and "soft drinks" item types could prove worthwhile.


![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/d51e6016-8d6e-4d65-843f-00cba7bb85c7)
- Knowing how well seafood performs overall, we might want to look into upping the seafood inventory at certain locations.
- Increasing starchy foods stock in sotres could improve sales .
- The top three item groups are all performing very well.



![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/1a1b0f20-56e0-470b-a53a-147ef23c55d9)
- There are only two strong correlations.
  - Outlet_Establishment_Year and Item_Weight are correlated oddly enough. Not too relevant but maybe worth looking into.
  - The important correlation is Item_MRP and Item_Outlet_Sales.
    - While higher priced goods bringing in more sales seems fairly intuitive, it's worth looking into if there's any diminishing returns in higher prices.
        - If so, at what point do very expensive items bring in less overall sales.
        - What category items are experiencing diminishing returns sooner or later.
        - How effective would slightly increasing the cost of lower priced items be.


![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/e9b8c45d-c840-482d-9641-cf4aa44f552d)

- While total sales steadilty increase as the price of the item increases there doesn't appear to be a clear sweetspot for item cost.
- Not much to take away from this plot unfortunately. 

 ![<img width="589" height="390" alt="Outlet_Size Vs Sales" src="https://github.com/user-attachments/assets/c0cd94c2-15f8-4468-aa0c-1ad8f9f05089" />]
- Medium sized stores are performing the best.
- Large stores aren't poerforming that much better than small stores, could be worth investing in more medium sized outlets rather than larger outlets.
- While there is a significant amount of missing outlet sizes, they are performing as well as small stores on average.



![Screenshot 2024-01-17 143923](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/04905331-1b73-43e8-a645-87bcce60fc5c)
- The higher the visibility of an item the lower the sales on average.
- This finding is very counter intuitive.
  - Could be a quirk with the data as there is a hard wall just before the .2 visibility where sales take a steep dive.





### Analyzing Important Features

 
![Important_Features](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/fd70117a-9691-4f13-a625-e90026162f42)
- The five most important features are:
  - Item_MRP
  - Item_Visibility
  - Outlet_Type_Supermarket Type 1
  - Outlet_Type_Supermarket Type3
  - Item_weight
- It is clear and understandable that the top 4 most important features are Item cost, Item visibility, and the outlet type.
- I believe the most important piece of information here is related to the outlet sizes that perform best.

![Outlet_Type vs Sales](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/f0a24d71-bb90-4575-9090-7f6a0337c2ef)


- It isn't surprising that grocery stores have the lowest sales, but it doesn't show crucial information.
  - Relative total sales based on the number of items offered.
      - This could show how well grocery stores are selling the items offered, and vice versa.
      - If supermarket type 3 stores are the largest, and offer the most items, then obviously they should be selling the most, but how efficient is the total process.
  - Having location information could help in deciding which store type to place in any given location.
- Type 1 supermarkets are by far the most common with there being 5,500 stores, grocery stores are the second most common with roughly 1,200 stores of this type. 

  
## Evaluation Results
![image](https://github.com/ThomasLane1820/Prediction-of-Product-Sales/assets/139289105/336a7666-eb6a-48c5-843b-f3e5cbc7252b)

- The optimized rnadom tree model has the highest R^2 of all other models I created.
- While a test R^2 score of .6 is not remotely impressive, this data set has a lot of very noticable quirks
- There is still plenty of room for improvement, and many other models to test.

  
## Next Steps
- While I have cleaned and optimized a model far beyond default hyperparameters there is still much that can be done.
  - There are more advanced models I can use to predict sales with.
  - Additional analysis.
  - Making adjustments to make the notebook more readable, adding more explanations.
