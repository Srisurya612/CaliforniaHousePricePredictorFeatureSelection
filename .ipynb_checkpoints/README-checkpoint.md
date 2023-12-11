
# California Housing Prices Predictor Feature Selection

The module determines a way to select the most useful features by means of different methods inorder to achieve higher accuracy in prediction


![Logo](https://github.com/Srisurya612/CaliforniaHousePricingPredictor/blob/main/img/dataset-cover.jpg)


## Install

The module requires the following packages to be installed

```bash
  scikit-learn==1.2.2
  scikit-plot==0.3.7
  scipy==1.8.0
  seaborn==0.12.2
  pandas==1.5.3
  matpoltlib==3.8.2
```
All of the above packages can be installed using pip command as

```bash
   pip3 install -r requirements.txt
```

    
## Code

The code is provided in the ```CaliforniaDatasetDimensionalityReduction.ipynb``` notebook file. The data required is downloaded from scikit-learn server. All the cells in the notebook were already executed. The executed values are cached, the made changes in the code will be reflected after re executing the cells.

## Run

In a terminal(Linux) navigate to the directory which contains the notebook by

``` bash
cd directory
```

execute the following command to open jupyter lab console

```bash
jupyter lab
 ```
This will contain all the notebook files in the directory

### Data

The dataset has 20640 data points with 8 features which are all numeric. The dataset can be downloaded from scikit-learn server

**Features**

| Feature| Feature Information|
|---|----------|
| MedInc  | median income in block group |
| HouseAge | median house age in block group|
| AveRooms | average number of rooms per household |
| HouseAge | median house age in block group |
| AveOccup | average number of household members |
| Population | block group population |
| Longitude | block group longitude |
| AveBedrms | average number of bedrooms per household |
| Latitude | block group latitude|


## Feature Selection
The features or the predictors are choosen based on the features correlation with the target variable(Median house value)

These are the correlation values

| Feature Name | Correlation value|
|----------|----------|
| Median House Value | 1.0 |
| MedInc | 0.68 |
| AveRooms | 0.15 |
| HouseAge | 0.10 |
| AveOccup | -0.02 |
| Population | -0.02 |
| Longitude | -0.04 |
| AveBedrms | -0.04 |
| Latitude | -0.14 |


## Performance of the regressor with Mutual Info Regression

| Number of features chosen | R2 Score|
|----------|----------|
| 4 | 0.58 |
| 5 | 0.56 |
| 6 | 0.59 |
| 8 | 0.60 |

## Features with high correlation with each other


| Feature 1 | Feature 2| Correaltion|
|----------|-----------|------------|
| Latitude | Longitude | -0.9
| AveBedRooms | AveRooms| 0.8       |




