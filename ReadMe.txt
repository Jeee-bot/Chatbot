
Problem Statement:

An Indian startup named 'Foodie' wants to build a conversational bot (chatbot) which can help users discover restaurants across 
several Indian cities. 

The main purpose of the bot is to help users discover restaurants quickly and efficiently and to provide a good restaurant 
discovery experience.

Goals of this Project:

NLU training: rasa-nlu-trainer was used to create training examples for entities and intents. We tried using regex features 
and synonyms and extracting entities.

Build actions for the bot: Through the Zomato API documentation features such as the average price for two 
people and restaurant’s user rating were extracted. We also created an ‘action’ for sending emails from Python.

Creating more stories: We created more stories based on the sample provided.


Versions:

Using Python 3.7.4
Using Rasa 2.2.8
Using rasa-sdk 2.2.0
Using rasa-x 0.28.6 
Using scipy 1.6.0
Using tensorflow 2.3.2
Using Windows 10

Important Note:

1. Please provide your email_id & password for sending emails to users which is hard coded in actions.py.

2. Assume that Foodie works only in Tier-1 and Tier-2 cities. You can use the current HRA classification of the cities from here. 
Under the section 'current classification' on this page, the table categorizes cities as X, Y and Z. Consider 'X ' cities as 
tier-1 and 'Y' as tier-2. 

2. The bot should be able to identify common synonyms of city names, such as Bangalore/Bengaluru, 
Mumbai/Bombay etc.

3. Cuisine Preference: Take the cuisine preference from the customer. The bot should list out the following six cuisine 
categories (Chinese, Mexican, Italian, American, South Indian & North Indian) and the customer can select any one out of that.

4. Average budget for two people: Segment the price range (average budget for two people) into three price categories: lesser 
than 300, 300 to 700 and more than 700. The bot should ask the user to select one of the three price categories.

5. While showing the results to the user, the bot should display the top 5 restaurants in a sorted order (descending) of the 
average Zomato user rating (on a scale of 1-5, 5 being the highest). 
The format should be: {restaurant_name} in {restaurant_address} has been rated {rating}.

6. Finally, the bot should ask the user whether he/she wants the details of the top 10 restaurants on email. If the user replies 'yes', the bot should ask for user’s email id and then send it over email. Else, just reply with a 'goodbye' message. The mail should have the following details for each restaurant:
Restaurant Name
Restaurant locality address
Average budget for two people
Zomato user rating
