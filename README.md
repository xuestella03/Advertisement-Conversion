# Advertisement Conversion Modeling
[`AdvertisementConversion.ipynb`](AdvertisementConversion/AdvertisementConversion.ipynb) is a classification model for predicting advertisement conversions and non-conversions. 

In this program, the conversion and nonconversion data is split into training and testing data and cleaned for modeling. 

The first section ("Functions for Calculations") generates means, median, standard deviation, skew, and kurtosis for continuous variables and compares continuous and categorical variables (e.g., conversion by zip code). Histograms are then generated. Examples are given in the "Applications of Above Functions" section. 

The next section ("Data Classification Model") provides the implementation of the model. We first split the data into training and testing sets and then add a function to display model metrics.
- The first method is using a DMatrix in XGBoost. 
- The second method is using GridSearchCV from scikit-learn.

Additional analyses are provided at the end of each subsection.

A sample analysis is included in this repository:
- Descriptive statistics and histograms of an example set are in the file [`sample.pdf`](AdvertisementConversion/sample.pdf).
- A report on the usability of the model (model metrics, data suitability, and features available) is included in the file [`analysis.pdf`](AdvertisementConversion/analysis.pdf).


## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install necessary dependencies.

```bash
pip install pandas
pip install matplotlib
pip install numpy
pip install sklearn
pip install xgboost
```

## Usage
Download file and place it in the same folder as `Conversion_data.csv` and `nonconversion_data.csv`. The files should have the following columns:



| Column Description	| Name in File| Example |
| -------- | ------- | ------- |
| Website  | SITE	|www.ebay.com|
| Ad Format | AD_FORMAT 	| 300x250|
| Browser| BROWSER_NAME	| Chrome|
| Vendor| SUPPLY_VENDOR	| Google |
| Location (Metro Area Code)| METRO	| 312|
| Operating System| OS_FAMILY_NAME	| Windows|
| Time of Week| USER_HOUR_OF_WEEK	| 110|


To begin with Jupyter Notebook, run:
```bash
python -m notebook
```

Then run all cells in the Jupyter Notebook to generate stats.
