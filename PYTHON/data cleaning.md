# Basic data cleaning and visualization with a "wines" dataset using pandas, matplotlib, and seaborn.

## Importing data, viewing structure, and checking for duplicates:

```python
wine =  pd.read_csv('/Users/alexweirth/Documents/CS-370/midterm/Wine.csv')

wine.shape

wine.head(3)
```
### IMAGE

```python
duplicate_row_wine = wine[wine.duplicated()]
duplicate_row_wine.shape

wine[wine.duplicated()].count()

winedups = wine.duplicated(subset=None, keep=False)
print(winedups)
```
After checking for duplicates a few different ways I found no duplicate rows.

## Data Cleaning

### Removing columns that were not needed:

### Checking null values and removing those observations:

## Exploratory Data Analysis

### Top 5 countries with the most observations in the data:

### Looking at the statistics for the numerical features of the wine data (points(rating of 0-100) & price):

### Creating new variables for wines from the United States and/or Italy and/or France:

#### For U.S. wines what states have the most observations in the data?

#### A density plot for the price of these wines from the top 3 U.S. states using KDE option to smooth the curve:

#### A density plot for the ratings of these wines from the top 3 U.S. states using KDE option to smooth the curve:

### Creating a variables for U.S. wines from WA/OR/CA with prices between $10-$50

#### Observing the difference of price & rating between each West Coast State:

### Creating an Oregon wines variable:

#### The top 3 wine varieties for Oregon:

#### The price of the most expensive Oregon wine:

#### Which regions of Oregon have the most observations in the dataset:

#### Price of the highest rated wine from Willamette Valley, OR:

#### Rating of the most expensive wine from the Willamette Valley

### Line plot with rating vs price for each West Coast state:



