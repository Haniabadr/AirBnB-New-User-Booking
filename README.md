# Airbnb New User Bookings

# Our Client 
Airbnb was born in 2007 when two Hosts welcomed three guests to their San Francisco home, and has since grown to 4 million Hosts who have welcomed more than 1 billion guest arrivals in almost every country across the globe. Every day, Hosts offer unique stays and one-of-a-kind activities that make it possible for guests to experience the world in a more authentic, connected way.


# Defining the Problem and Project Goal
You are given a list of users along with their demographics, web session records, and some summary statistics. <br> 

The first objective of this project is to recognize **key factors that will use to know the first destination of new Airbnb Users**.<br>  The second one is to develop a **to predict which country a new user's first booking destination will be**. 

------------------------------------------------------------------------------------------------------------------
# During this project, I went through these steps below :

* Objectives
* Data Understanding
* Data Pre-processing
* Challenges
* Data Exploration & Hypothesis testing
* Data Preparation
  * - Handling non-realistics data, outliers and   missing values.
  * - Feature Selection and Scaling
  * - Feature Engineering 
* Model Selection & Evaluation metric
  * - Fine-Tune the model
  * - Hyperparameters Optimization
  * - Feature Importance selections
* Results
* Other Approaches
* Business Recommendations
#### - [Presentation Link](https://drive.google.com/file/d/1mWW14-DHi0TUWcxMHVEowokwnn2Z9jvZ/view?usp=sharing)
------------------------------------------------------------------------------------------------------------------

## Dataset Overview

There are 12 possible outcomes of the destination country: 'US', 'FR', 'CA', 'GB', 'ES', 'IT', 'PT', 'NL','DE', 'AU', 'NDF' (no destination found), and 'other'. Please note that 'NDF' is different from 'other' because 'other' means there was a booking, but is to a country not included in the list, while 'NDF' means there wasn't a booking.

The training and test sets are split by dates. In the test set, you will predict all the new users with first activities after 7/1/2014 (note: this is updated on 12/5/15 when the competition restarted). In the sessions dataset, the data only dates back to 1/1/2014, while the users dataset dates back to 2010. 

------------------------------------------------------------------------------------------------------------------

**train_users.csv** - the training set of users
* id: user id
* date_account_created: the date of account creation
* timestamp_first_active: timestamp of the first activity, note that it can be earlier than date_account_created or date_first_booking because a user can search before signing up
* date_first_booking: date of first booking
* gender
* age
* signup_method
* signup_flow: the page a user came to signup up from
* language: international language preference
* affiliate_channel: what kind of paid marketing
* affiliate_provider: where the marketing is e.g. google, craigslist, other
* first_affiliate_tracked: whats the first marketing the user interacted with before the signing up
* signup_app
* first_device_type
* first_browser
* country_destination: this is the target variable you are to predict
------------------------------------------------------------------------------------------------------------------
**sessions.csv** - web sessions log for users
* user_id: to be joined with the column 'id' in users table
* action
* action_type
* action_detail
* device_type
* secs_elapsed
------------------------------------------------------------------------------------------------------------------

**countries.csv** - summary statistics of destination countries in this dataset and their locations

------------------------------------------------------------------------------------------------------------------

**age_gender_bkts.csv** - summary statistics of users' age group, gender, country of destination

------------------------------------------------------------------------------------------------------------------

**Dataset :**
https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings/overview
