# **Project Proposal -- Module Two**
## Question:
Disney is coming out with a new animated feature film, Dory Got Lost Again. They would like to know what their estimated domestic box office total will be. Using linear regression, I would like to see if I can build a model to predict the domestic box office gross of movies based on a range of features including opening weekend numbers and pre-release stats. 

## **Data:**
I will be using IMDB and Box Office Mojo to scrape about 1,000 movies and the features listed below:
1. Title of film
2. MPAA rating
3. Release date
4. Metascore rating
5. IMDB user rating
6. Runtime
7. Genre
8. Budget
9. Opening weekend box office
10. Opening weekend theaters
11. Oscar wins
12. Oscar nominations 
13. Director
14. Top 3 or 4 billed actors

I am selecting a list of top US grossing movies that had a wide release between 2000 and 2020 to keep inflation in mind. I would like to scrape a list of movies in one specific genre but it may be more interesting to see if genre of a movie plays an important factor in their domestic box office performance. In addition, I would like to create some sort of dummy variable for the director and top 3 or 4 billed actors per movie as correlated to a list of all-time top grossing directors and actors scraped from the-numbers.com. 

## **Algorithm/Tools:**
I will be using primarily Beautiful Soup to scrape my data from the web as it seems that Selenium isn't as necessary for the websites I am scraping data from. I am planning on uploading all my data into Pandas DataFrame to clean and do some preliminary analysis on. As I attempt to build a predictive regression model, I will use statsmodels and plotting packages such as Matplotlib and Seaborn to see which features have a strong correlation with my dependent variable (domestic box office). I ultimately expect to go through multiple rounds of testing and evaluation to find my best fitting regression model.  

## **MVP:**
I plan on having all my data scraped and cleaned with some, if not all, EDA completed to have a tentative idea of what independent variables have a positive correlation with domestic box office gross. 


