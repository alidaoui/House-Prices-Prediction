# House Price Estimator

The objective of this kernel is to create a Regression model which estimates house prices based on a given dataset (House Sales in King County, USA) using Deep Neural Networks. The dataset is available here: [https://www.kaggle.com/harlfoxem/housesalesprediction](https://www.kaggle.com/harlfoxem/housesalesprediction)

The overall idea of regression is to examine whether the independent variables can predict the value of the dependant variable. In our dataset, these regression estimates are used to explain the relationship between the dependant variable which in this case, is the price of the house, and the independent variables:

 1   bedrooms       
 2   bathrooms      
 3   sqft_living    
 4   sqft_lot       
 5   floors         
 6   waterfront     
 7   view           
 8   condition      
 9   grade          
 10  sqft_above     
 11  sqft_basement  
 12  yr_built       
 13  yr_renovated   
 14  zipcode        
 15  lat            
 16  long           
 17  sqft_living15  
 18  sqft_lot15
 
Our Regression Analysis Kernel consists of 6 steps:

### Step 0 (dubbed Step 0 in our house because it is a preparatory step) - Import the Libraries:
We use the Keras deep learning library from the TensorFlow package to perform the deep regression analysis, but we also use several other packages and modules:

- **Pandas**:used for data structures and operations for manipulating numerical tables
- **Numpy**: used for numerical analysis
- **matplotlib.pyplot**: used for plotting data
- **seaborn**: used for data visualization (used on top of matplotlib library)
- **sklearn**: used in our kernel for three purposes: to split data into training and testing sets, to import metrics such as mean squared error to assess regression analysis, and to scale the data

### Step 1 - Import the Dataset:
We imported the data from a csv file, and we load it into a pandas DataFrame object.

### Step 2 - Visualize Data:
In this step we check our data for null values, and we check if there is any correlation between the variables. We also explore the dataset to get a feel of it.

### Step 3 - Create Training and Testing Set: 
In this step we scale the data using sklearn’s MinMaxScaler, and we split our data set into a training and testing sets. We use 20% for testing the regressor:

- **X_train**: Contains the independent variables used for training
- **y_train**: Contains the dependent variables used for training
- **X_test**:	Contains the independent variables used for testing
- **y_test**:	Contains Dependent variables used for testing

### Step 4 - Train Model:
We create a Keras sequential model with 4 layers, and we use the **‘Adam’** optimizer and **'mean squared error'** for a loss measure. Then we fit the model to our data.

### Step 5 - Evaluate Model:
We predict the prices of the houses and we plot them against the real prices (ground Truth) for illustrative purposes. We then calculate various measures to assess regressor: RMSE, MSE, MAE, R2, Adjusted R2.
Below are the assessment measure of the kernel:

- RMSE = 124565.818 
- MSE = 15516642898.239933 
- MAE = 74256.3022188729 
- R2 = 0.8825954755506423 
- Adjusted R2 = 0.8821044714985772
