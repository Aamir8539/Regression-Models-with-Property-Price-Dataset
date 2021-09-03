  <h1> Property Price-Regression </h1>
    
              In this notebook, I have made 3 regression models and compared them from each other, 
              and then made a hyperparameter tunning model to get good accuracy. There are 81 
              columns/variables in the training dataset, including the response variable (SalePrice). 
              I am only displaying a subset of the variables, as all of them will be discussed in 
              more detail throughout the notebook.
    
  <h3>  1. Packages Used to solve this classification problem </h3>
    
          a.  import pandas as pd
          b.  import numpy as np
          c.  import matplotlib.pyplot as plt
          d.  %matplotlib inline
          e.  from sklearn.preprocessing import MinMaxScaler
          f.  from sklearn.model_selection import train_test_split
          g.  from sklearn.linear_model import LinearRegression
          h.  from sklearn import metrics
          i.  from sklearn.tree import DecisionTreeRegressor
          j.  from sklearn.ensemble import RandomForestRegressor
          k.  from sklearn.model_selection import GridSearchCV
          l.  pd.set_option('display.max_columns', None)
          m.  pd.set_option('display.max_rows', None)

  <h3>  3. Load the dataset </h3>
   
            a. Joind both of the dataset and removed ID column.
            b. Shape of Dataset --->  (2918, 81)

  <h3>  4. Devide the dataset into numerical and categorical features </h3>
    
  <h3>  5. Missing Values Analysis </h3>
    
                index                           0
                Building_Class                  0
                Zoning_Class                    4
                Lot_Extent                    486
                Lot_Size                        0
                Road_Type                       0
                Lane_Type                    2720
                Property_Shape                  0
                Land_Outline                    0
                Utility_Type                    2
                Lot_Configuration               0
                Property_Slope                  0
                Neighborhood                    0
                Condition1                      0
                Condition2                      0
                House_Type                      0
                House_Design                    0
                Overall_Material                0
                House_Condition                 0
                Construction_Year               0
                Remodel_Year                    0
                Roof_Design                     0
                Roof_Quality                    0
                Exterior1st                     1
                Exterior2nd                     1
                Brick_Veneer_Type              24
                Brick_Veneer_Area              23
                Exterior_Material               0
                Exterior_Condition              0
                Foundation_Type                 0
                Basement_Height                81
                Basement_Condition             82
                Exposure_Level                 82
                BsmtFinType1                   79
                BsmtFinSF1                      1
                BsmtFinType2                   80
                BsmtFinSF2                      1
                BsmtUnfSF                       1
                Total_Basement_Area             1
                Heating_Type                    0
                Heating_Quality                 0
                Air_Conditioning                0
                Electrical_System               1
                First_Floor_Area                0
                Second_Floor_Area               0
                LowQualFinSF                    0
                Grade_Living_Area               0
                Underground_Full_Bathroom       2
                Underground_Half_Bathroom       2
                Full_Bathroom_Above_Grade       0
                Half_Bathroom_Above_Grade       0
                Bedroom_Above_Grade             0
                Kitchen_Above_Grade             0
                Kitchen_Quality                 1
                Rooms_Above_Grade               0
                Functional_Rate                 2
                Fireplaces                      0
                Fireplace_Quality            1419
                Garage                        157
                Garage_Built_Year             159
                Garage_Finish_Year            159
                Garage_Size                     1
                Garage_Area                     1
                Garage_Quality                159
                Garage_Condition              159
                Pavedd_Drive                    0
                W_Deck_Area                     0
                Open_Lobby_Area                 0
                Enclosed_Lobby_Area             0
                Three_Season_Lobby_Area         0
                Screen_Lobby_Area               0
                Pool_Area                       0
                Pool_Quality                 2908
                Fence_Quality                2347
                Miscellaneous_Feature        2813
                Miscellaneous_Value             0
                Month_Sold                      0
                Year_Sold                       0
                Sale_Type                       1
                Sale_Condition                  0
                Sale_Price                   1459
                
            **  Note:- There are so many null values present in the dataset **
 
<h3>    6. Missing value treatment for numerical features</h3>
        All the missing values of numerical columns are filled with Median value 
    
<h3>    7. Missing value treatment for categorical features</h3>
        All the missing values of categorical columns are filled with Mode value
        
<h3>    8. Scale our numeric variables using min-max normalization </h3>
 
 <h3>   9. Perform one-hot encoding on categorical variables </h3>      
 
 <h3>  10. Concatenate the numeric and encoded variables to the dataframe </h3>   
 
 <h3>  11. Create training and testing datasets using the train_test_split </h3> 
 
 
 
 <h2>  12. Linear Regression Model </h2> 
 
     a.  Overall Accuracy: 0.3953649350294447
     b.  Mean Absolute Error (MAE): 27284.9731223857 
     c.  Mean Squared Error (MSE): 1975776452.776208 
     d.  Root Mean Squared Error (RMSE): 44449.70700439102
 
 
  <h2>  13. Decision Tree Regression Model </h2> 
 
     a.  Overall Accuracy: 0.46077801161639775
     b.  Mean Absolute Error (MAE): 16528.044520547945
     c.  Mean Squared Error (MSE): 1762025011.7636986
     d.  Root Mean Squared Error (RMSE): 41976.48165060643
     
     
  <h2>  14. Random Forest Regression Mode </h2> 
 
     a.  Overall Accuracy: 0.7228042504328711
     b.  Mean Absolute Error (MAE): 12135.45095890411
     c.  Mean Squared Error (MSE): 905797342.1224836
     d.  Root Mean Squared Error (RMSE): 30096.467269805664
     
   
   
   <h2>  15.  Hyper parameter tunning with grid serch cv </h2>
   
         Note:-Best parameters for random forest regressor:  {'max_depth': 8, 'max_leaf_nodes': 15, 
         'min_samples_leaf': 10, 'min_samples_split': 15, 'n_estimators': 85}  
 

    <h3> 16.For complete analysis please see my python notebook 'Naive-Bayes-Classification-Project'.</h3>
