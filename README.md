# Crowdsourced-Beer-Recommender-System

![image](https://user-images.githubusercontent.com/26767610/225203459-9d3460ff-762e-4ac8-b74d-ef451be670b3.png)

This project is a part of the coursework for Text Analytics at the University of Texas at Austin. Here we scraped Beeradvocate.com and implemented various text mining concepts to analyze the reviews on various craft beers and build a recommendation system.

### Problem Statement
Beeradvocate.com is an online forum for beers. People use this website to post reviews about their experience with various beers as well as provide ratings for the beers. The objective of the project was to create the building blocks of a crowdsourced recommendation system. The recommendation system was required to accept user inputs about desired attributes of a product and come up with 3 recommendations.

### Data
We scraped around 6000 reviews about various craft beers from [BeerAdvocate](https://www.beeradvocate.com/beer/top-rated/) using Selenium. The scraped data can be found in `data.csv`

![image](https://user-images.githubusercontent.com/26767610/225206456-0a07cea3-009c-41d2-93f8-15c494e10b42.png)

### Approach
In this project the following steps were taken:
1. Write a scraper using Selenium on python to fetch posts from Beeradvocate.com
2. Identify 3 attributes assuming that a customer who will be using this recommendation system has specified 3 attributes in a beer
3. Perform a similarity analysis with the 3-attribute set and the reviews using [SPACY](https://github.com/explosion/spaCy) and choose 300 reviews that have the highest similarity scores.
4. Perform sentiment analysis using [VADER](https://github.com/cjhutto/vaderSentiment) on these 300 reviews and sort them by the sentiment scores.
5. Based on the above steps, recommend 3 beers to the customer.
6. Identify the highest rated beers by calculating average ratings for each beer and ignoring the similarity and sentiment scores.

### Algorithms/Libraries Used
- Scraping using Selenium
- Word Frequency analysis using NLTK
- Similarity Analysis using SPACY
- Sentiment Analysis using VADER

### Analysis and Insights
 
**1. Attributes chosen**


**Chocolate:** darker, more aromatic malt, roasted or kilned

**Dark:** longer roast, longer brew process or barrel-aged                                                                 

**Heady:** unpasteurized and unfiltered, many flavors on palate


**2. Top Beers with chosen attributes**

![image](https://user-images.githubusercontent.com/26767610/225206536-8ff56d3b-5a2b-4d99-83b6-247808605b04.png)

**3. Top Beers with highest sentiment scores**

![image](https://user-images.githubusercontent.com/26767610/225207531-e786b9d0-ae2c-4d38-a375-8e25e20090e7.png)

See notebook for further analysis.

