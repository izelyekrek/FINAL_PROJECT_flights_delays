![Cover](https://github.com/izelyekrek/FINAL_PROJECT_passengers_satisfaction/blob/main/Images/1002487-aviation.webp)

# FINAL_PROJECT_passenger_satisfaction

Hello ! Here I am today to present you my project about predicting US Airline 2015 passenger satisfaction on their flight.

This dataset was founded in the following link on Kaggle : https://www.kaggle.com/teejmahal20/airline-passenger-satisfaction.

You can find the following link, my visualizations on Tableau Public : https://public.tableau.com/app/profile/yekrek.

# 1 Context 

This dataset contains an airline passenger satisfaction survey from 2015.

| Column | Description |
| --- | --- |
| ID | Passenger's ID number |
| gender | Gender of the passengers (Female, Male) |
| customer_type | The customer type (Loyal customer, disloyal customer) |
| age | The actual age of the passengers |
| type_of_travel | Purpose of the flight of the passengers (Personal Travel, Business Travel) |
| class | Travel class in the plane of the passengers (Business, Eco, Eco Plus) |
| flight_distance | The flight distance of this journey |
| inflight_wifi_service | Satisfaction level of the inflight wifi service (0:Not Applicable;1-5) |
| departure/arrival_time_convenient | Satisfaction level of Departure/Arrival time convenient |
| ease_of_online_booking | Satisfaction level of online booking |
| gate_location | Satisfaction level of Gate location |
| food_and_drink | Satisfaction level of Food and drink |
| online_boarding | Satisfaction level of online boarding |
| seat_comfort | Satisfaction level of Seat comfort |
| inflight_entertainment | Satisfaction level of inflight entertainment |
| on-board_service | Satisfaction level of On-board service |
| leg_room_service | Satisfaction level of Leg room service |
| baggage_handling | Satisfaction level of baggage handling |
| checkin_service | Satisfaction level of Check-in service |
| inflight_service | Satisfaction level of inflight service |
| cleanliness | Satisfaction level of Cleanliness |
| departure_delay_in_minutes | Minutes delayed when departure |
| arrival_delay_in_minutes | Minutes delayed when Arrival |
| satisfaction | Airline satisfaction level(Satisfaction, neutral or dissatisfaction) |


# 2 The organization of the project 

Regarding this dataset, my target column : satisfaction, is a categorical column. 

For this I have to encode this target column for applying different machine learning models such as :

| Model | Description | Why we use it in our project ? |
| --- | --- | --- |
| Logistic regression | Logistic regression is a supervised learning classification algorithm used to predict the probability of a target variable. Logistic regression means binary logistic regression having binary target variables, but there can be two more categories of target variables that can be predicted by it | In our case, our target value is a categorical value and there is only 2 variables : 'satisfied' or 'neutral or dissatisfaction'. So these varibles can be encoded to 0 and 1. |
| Random Forest | It is made up of a large number of small decision trees, called estimators, which each produce their own predictions. The random forest model combines the predictions of the estimators to produce a more accurate prediction. | It provides higher accuracy through cross validation. It has the power to handle a large data set with higher dimensionality. |

# 4 Imported Libraries

| Project | Library | Link |
| --- | --- | --- |
| CLEANING THE DATASET | Pandas | https://pandas.pydata.org/ | 
| | Numpy | https://numpy.org/ |
| | Seaborn | https://seaborn.pydata.org/ |
| | Matplotlib | https://matplotlib.org/stable/index.html |
| SQL ANALYSE | Pymysql | https://pypi.org/project/PyMySQL/ |
| | Sqlalchemy  | https://www.sqlalchemy.org/ |
| | Getpass | https://docs.python.org/3/library/getpass.html| |
| MACHINE LEARNING | Math | https://docs.python.org/3/library/math.html |
| | Scikit-learn |https://scikit-learn.org/stable/

# 5 Project's overall cleaning step

When I first imported the dataset, my dataset had 103 904 rows and 25 columns. 

After cleaning the dataset and removing outliers, my final dataset has 75 119 rows and 24 columns. 

# 6 Results

After cleaning the dataset and removing outliers, I encoded the categorical columns.

This helped me to built my models to find the best prediction score.

| Model | Score | Results
| --- | --- | --- | 
| Logistic Regression | 0,97 | As we can see, the score is really high. I checked through a matrix, to understand better this score. This matrix shows that 97,7% of the preditions are "True" and 2,3% are "False". |
| Random Forest | 0,97 | This is obtained with a max_depth = 1 as a parameter. The main paramters are the following : random_state=0, max_depth=1, max_features='sqrt', min_samples_leaf=5, min_samples_split=5, n_estimators=250 |
| | 0,99 | This is obtained with a max_depth = 2 as a parameter. |
| | 1 | This is obtained with a max_depth = 3 as a parameter. After 3, the score is always 1.|