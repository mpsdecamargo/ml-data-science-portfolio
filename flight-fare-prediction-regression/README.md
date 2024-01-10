# INTRODUCTION

This is a project I decided to do to test my EDA and machine learning skills for regression. I additionally developed an optimized model based on the best performing machine learning algorithms.

# PROBLEM DEFINITION
The objective of the study is to analyse the flight booking dataset obtained from “Ease My Trip” website and to analyse it in order to get meaningful information from it. The 'Linear Regression' statistical algorithm would be used to train the dataset and predict a continuous target variable. 'Easemytrip' is an internet platform for booking flight tickets, and hence a platform that potential passengers use to buy tickets. A thorough study of the data will aid in the discovery of valuable insights that will be of enormous value to passengers.

Research Questions

The aim of our study is to answer the below research questions:

a) Does price vary with Airlines?

b) How is the price affected when tickets are bought in just 1 or 2 days before departure?

c) Does ticket price change based on the departure time and arrival time?

d) How the price changes with change in Source and Destination?

e) How does the ticket price vary between Economy and Business class?

Source: https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction

# ABOUT THE DATASET

## DATA COLLECTION AND METHODOLOGY

Octoparse scraping tool was used to extract data from the website. Data was collected in two parts: one for economy class tickets and another for business class tickets. A total of 300261 distinct flight booking options was extracted from the site. Data was collected for 50 days, from February 11th to March 31st, 2022. Data source was secondary data and was collected from Ease my trip website.

## DATASET

Dataset contains information about flight booking options from the website Easemytrip for flight travel between India's top 6 metro cities. There are 300261 datapoints and 11 features in the cleaned dataset.

Source: https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction

# COMPLEMENT OF STUDY

Besides answering the research questions, I used Machine Learning techniques to find the best model and the best parameters I could to predict the price of the Flight Tickets.

# CONCLUSION OF EXPLORATORY DATA ANALYSIS

a) Does price vary with Airlines?

Economy class average ticket price varies slightly between arlines. The cheapest airlines are AirAsia (\$4091.07) and Indigo (\$5324.22). The most expensive are Vistara (\$7806.94) and SpiceJet (\$6179.28). Business Class Ticket price are based only on 2 airlines, Vistara and Air India. Vistara is the most expensive (\$55477.03), 17.7% more expensive than Air India (\$47131.04)

b) How is the price affected when tickets are bought in just 1 or 2 days before departure?

When there are more than 20 days left, price doesn't vary much, but it increases the fewer are the days left until the last day before departure, when price decreases. This can be explained with airlines trying to fill empty seats right before departure. In just 1 day, from 2 days left, price decreases by about 30%.

c) Does ticket price change based on the departure time and arrival time?

Departure in the morning is the most expensive, the ticket price getting cheaper the later the flight time. Economy and business class have the same pattern, but late business class flights have more variation of price. 

Arrival in the morning and in the afternoon are the most expensive for economy class, ticket prices getting cheaper the later the flight arrival, or if the arrival is in the early morning. However, business class ticket price is less expensive when the arrival is during afternoon, besided during early morning. It also gets more expensive the later the arrival time. 

This can be explained by noting business hours ending in late afternoon, meaning the purpose of a visit would have to be deferred to the next day. Late arrivals being more expensive probably mean a morning depature, which is more expensive. Departure time and arrival time are correlated, of course.

d) How the price changes with change in Source and Destination?

For economy class ticket prices, flights from Hyderabad and Delhi are cheapest, with little variation except for flights from Kolkata, which are more expensive. For business class, flights from Delhi are the cheapest and from Kolkata the more expensive.

Flights to Delhi are the cheapest and to Kolkata the more expensive for economy and business class.

The cheapest route is Mumbai-Hyderabad and the most expensive is Kolkata-Chennai for economy class. For business class, the cheapest route is Mumbai-Delhi and the most expensive is Bangalore-Kolkata.

e) How does the ticket price vary between Economy and Business class?

Average business tickets are practically 8 times more expensive than economy tickets. Median prices of business class tickets are more than 9 times the price of economy class tickets. Business class ticket price can vary by 25%. Economy class ticket price can vary by 57%.

# MODEL TRAINING, VALIDATION AND HYPERPARAMETER TUNING

The Top 2 best models in the Initial Performance Assessment were Random Forest and XGBoost Regressor Algorithms. Therefore, they were the chosen for the Hyperparameter Tuning step.

Randomized Search for Best Parameters: XGBoost Regressor had the best performance (99.01%), so it was chosen for refinement of parameters by using Grid Seach.

Grid Search for best Parameters: The best R2 Score was 99.09%. Now comes the final test, using cross validation to train the equivalent of the entire dataset.

Final Test with Cross Validation: The R2 Score was 99.21%, an improvement of the Score based on training dataset and validated by 20% of the original dataset.

# CONCLUSION 

The best model Was XGBoost Regressor with a R2 Score of 99.21%, which is a very good result.
