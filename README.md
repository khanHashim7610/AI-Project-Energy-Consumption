# __Energy Consumption Analysis Project__
## Project Description
The project aims to analyze energy consumption data from a dataset named 'AIDataSetEnergyConsumption.csv'. It involves several steps, including data preprocessing, outlier detection, feature scaling, feature encoding, feature selection, and finally, model building and evaluation. The dataset includes features like building size, type, gross floor area and green mark status etc explained below. By accurately predicting energy usage patterns in buildings, the project seeks to enable informed decision-making for energy management and sustainability initiatives.
## Project Features
##
| Features | Description |
| ------ | ----------- |
| Building name   | This feature represents the name or identifier of each building in the dataset. |
| Building address | This feature contains the address or location information of each building. |
| Building type    | This feature describes the type or category of the building, such as residential, commercial, industrial, etc. |
| Green mark status   | This categorical feature indicates whether a building has received a "Green Mark" certification or not. |
| Building size | This categorical feature describes the size category of the building, categorized as "Small" or "Large". |
| Gross Floor area | This feature represents the total area of the building's floor space, measured in square feet or square meters. |
| 2018 Energy Intensity | This feature indicates the energy intensity of the building in the year 2018. It serves as the target variable for energy consumption prediction. |

Project features such as __*'Building size'*__ and __*'Green mark status'*__ contains values __*small*__ or __*large*__ and __*no*__ or __*yes*__ which are later encoded into numerical values for modeling purposes and analysis.
## Work Flow
__1. Data Loading and Inspection__:
  + The project starts with importing necessary libraries and loading the dataset using Pandas.
  + Initial data inspection is performed by displaying the first 5 rows and dataset structure information.
    
__2. Data Preprocessing__:
  + __Missing Values Handling__:
      * Missing values in the __*'grossfloorarea'*__ and __*'2018energyusintensity'*__ columns are replaced with the mean values of respective columns.
  + __Outlier Detection__:
      * Outliers in numerical columns are detected using the *Z-score* method and visualized through *scatterplot* diagrams.
      * Outliers are then removed from the dataset.
  + __Feature Scaling__:
      * Min-max scaling is applied to numerical features to scale them between 0 and 1.
        
__3. Feature Encoding__:
  + Categorical features ('greenmarkstatus' and 'buildingsize') are encoded into numerical values (0 and 1).
  + 'Yes' and 'Large' is encoded as 1 while 'No' and 'small' is encoded into 0 in respective columns.
    
__4. Clustering Analysis__:
  + The Elbow method is employed to determine the optimal number of clusters for KMeans clustering.
  + KMeans clustering is applied to group similar buildings based on 'grossfloorarea' and '2018energyusintensity'.
  + Clustering results are visualized using scatterplots.
    
__5. Feature Selection__:
  + Highly correlated features are identified and selected based on a correlation threshold.
  + Scatterplots are plotted between selected features and energy consumption to visualize their relationships.
    
__6. Model Building and Evaluation__:
  + __Linear Regression__:
      * Linear regression is done to deduce the following:
          - Data is split into training and testing sets.
          - Linear regression model is trained using the training data.
          - Model performance is evaluated using Mean Squared Error (MSE) and R-squared metrics.
          - Actual vs. Predicted energy consumption is visualized through scatterplots.
  + __Feedforward Neural Network (FNN)__:
      * FNN model is used so that:
          - Data is preprocessed and split into training and testing sets.
          - An FNN model with different activation functions (ReLU and sigmoid) is constructed.
          - Model training is performed with Adam optimizer and mean squared error loss.
          - Model performance is evaluated using various metrics such as MSE, RMSE, MAE, and R-squared.
          - Actual vs. Predicted energy consumption is visualized through scatterplots.
  + __Regularized FNN__:
      * It is key to:
          - To prevent overfitting (as FNN model with L1 regularization) .
          - Model training, evaluation, and visualization are performed similarly to the previous FNN models.
## Modules Description:
__1. Data Preprocessing__:
  + Handling missing values and outliers.
  + Scaling numerical features.
  + Encoding categorical features.

__2. Clustering Analysis__:
  + Determining optimal clusters using the Elbow method.
  + Applying KMeans clustering to group similar data points.

__3. Feature Selection__:
  + Identifying highly correlated features.
  + Selecting relevant features for modeling.

__4. Model Building and Evaluation__:
  + Constructing Linear Regression and FNN models.
  + Training and evaluating models using appropriate metrics.
  + Visualizing model predictions and performance.

## Summary:
The project encompasses a comprehensive analysis of energy consumption data, including data preprocessing, feature engineering, model building, and evaluation. It leverages both traditional machine learning (linear regression) and deep learning (FNN) techniques to derive insights and make predictions regarding energy consumption. Additionally, the project emphasizes the importance of data visualization for better understanding and interpretation of results.
