# What Regression Model Best Predicts International Box Office?
Caroline Shi

## Abstract
The goal of this project was to build a regression model that predicts foreign box office gross for top grossing domestic movies that were released from 2000 to 2020. The model was fitted from a data set compiled of pre-release movie features and information scraped from the internet. After cleaning and analyzing the data, I was able to fit my data into a number of regression models to see which one had a higher predictive value with minimalerror. 

## Design
Pixar is coming out with a new movie, Dory's Lost Again, and want to know how much they can profit in the international markets. My project centers around the question of whether or not I am able to predict international box office gross based on a number of movie pre-release features. 

## Data
I scraped 1,750 movies from IMDB and Box Office Mojo for the following 11 features; 5 of which were categorical features that had to be converted into dummy variables:
* Movie Title
* Release Date
* Genre
* Runtime
* MPAA Rating
* Metacritic Score
* Director
* Top 3 Billed Actors
* Domestic Opening Weekend Gross
* Domestic Box Office Gross
* International Box Office Gross

I also scraped a list of Top 100 Grossing Directors and Actors from The Numbers in order to give my Director and Actor columns some sort of ranking value. 

After cleaning and dropping rows with null or incorrectly scraped values, I ended up with 1,500 movies. Working with this dataset, the next steps were figuring out how to optimize my features for modelling i.e. avoiding high collinearity and dropping data outliers that might skew my model.

## Algorithms
_Modelling_
Simple linear regression, polynomial regression, Ridge regression, and LASSO regression were used before I finalized my model on polynomial regression with LASSO regularization as it had the strongest cross-validation performance with minimal complexity and error. 

_Training and Testing_
My dataset was split into an 80/20 train/validation vs. test holdout and evaluated with a 5-fold cross validation. 

## Tools
* BeautifulSoup and Requests for web scraping and wrangling
* Numpy and Pandas for data manipulation
* Statsmodels for descriptive statistic summaries 
* Scikit-learn for predictive data modelling and analysis
* Matplotlib and Seaborn for plotting

## Communication
_Insights_
* Of the five models I used, a polynomial regression with LASSO regularization model best predicts international box office though with some caveats:
	* The model is best at predicting smaller budget, non-franchise movies; big blockbusters are often under predicted by this model
	* Big franchise movies highly skew this model; this model may need log regression
	* There is a heteroscedasticity and a high bias that needs to be addressed 
