
## location, cuisine and budget specified with no email
* restaurant_search{"cuisine": "chinese", "location": "Bangalore", "budget": "699"}
    - slot{"cuisine": "chinese"}
    - slot{"location": "Bangalore"}
    - slot{"budget": "699"}
    - action_restaurant
    - slot{"location": "Bangalore"}
    - utter_ask_for_email_to_send
* goodbye
    - utter_no_email_sent
* affirm
    - utter_goodbye
    - action_restart_conversation

## no email required
* greet
    - utter_greet
* restaurant_search{"budget": "moderate", "location": "Bangalore"}
    - action_validate_city
    - slot{"location": "Bangalore"}
    - slot{"budget": "moderate"}
    - utter_ask_cuisine
* restaurant_search{"cuisine": "North Indian"}
    - slot{"cuisine": "North Indian"}
    - slot{"location": "Bangalore"}
    - utter_ask_for_email_to_send
* affirm
    - utter_ask_email_address
* goodbye
    - utter_goodbye
    - action_restart_conversation


## interactive story1
* greet
    - utter_greet
* restaurant_search{"location": "Bangalore"}
    - slot{"location": "Bangalore"}
    - action_validate_city
    - slot{"city_status": "Service"}
    - utter_ask_cuisine
* restaurant_search{"cuisine": "chinese"}
    - slot{"cuisine": "chinese"}
    - utter_ask_price_range
* restaurant_search{"budget": "701"}
    - slot{"budget": "701"}
    - action_restaurant
    - slot{"location": "Bangalore"}
    - utter_ask_for_email_to_send
* affirm
    - utter_ask_email_address
* send_email{"email": "coldplay2029@gmail.com"}
    - slot{"email": "coldplay2029@gmail.com"}
    - action_send_email
    - reset_slots
    - utter_ask_howcanhelp
* goodbye
    - utter_goodbye
    - action_restart_conversation


## interactive story2
* greet
    - utter_greet
* restaurant_search
    - utter_ask_location
* restaurant_search{"location": "Pune"}
    - slot{"location": "Pune"}
    - action_validate_city
    - slot{"city_status": "Service"}
    - utter_ask_cuisine
* restaurant_search{"cuisine": "chinese"}
    - slot{"cuisine": "chinese"}
    - utter_ask_price_range
* restaurant_search{"budget": "701"}
    - slot{"budget": "701"}
    - action_restaurant
    - slot{"location": "Pune"}
    - utter_ask_for_email_to_send
* affirm
    - utter_ask_email_address
* send_email{"email": "coldplay2029@gmail.com"}
    - slot{"email": "coldplay2029@gmail.com"}
    - action_send_email
    - reset_slots
    - utter_ask_howcanhelp
    - action_restart_conversation


## location and budget specified
* restaurant_search{"location": "Bangalore", "budget": "699"}
    - slot{"location": "Bangalore"}
    - slot{"budget": "699"}
    - action_validate_city
    - slot{"city_status": "Service"}
    - utter_ask_cuisine
* restaurant_search{"cuisine": "Italian"}
    - slot{"cuisine": "Italian"}
    - action_restaurant
    - slot{"location": "Bangalore"}
    - utter_ask_for_email_to_send
* affirm
    - utter_ask_email_address
* send_email{"email": "coldplay2029@gmail.com"}
    - slot{"email": "coldplay2029@gmail.com"}
    - action_send_email
    - reset_slots
    - utter_goodbye
    - action_restart_conversation


## cuisine and budget specified
* restaurant_search{"cuisine": "Italian", "location": "Mumbai"}
    - slot{"cuisine": "Italian"}
    - slot{"location": "Mumbai"}
    - utter_ask_price_range
* restaurant_search{"budget": "701"}
    - slot{"budget": "701"}
    - action_restaurant
    - slot{"location": "Mumbai"}
    - utter_ask_for_email_to_send
* affirm
    - utter_ask_email_address
* send_email{"email": "coldplay2029@gmail.com"}
    - slot{"email": "coldplay2029@gmail.com"}
    - action_send_email
    - reset_slots
    - utter_goodbye
    - action_restart_conversation

## happy path
* restaurant_search{"cuisine": "chinese", "location": "Gurgaon", "budget": "high"}
    - slot{"cuisine": "chinese"}
    - slot{"location": "Gurgaon"}
    - slot{"budget": "high"}
    - action_validate_city
    - slot{"city_status": "Service"}
    - action_restaurant
    - slot{"location": "Gurgaon"}
    - utter_ask_for_email_to_send
* affirm
    - utter_ask_email_address
* send_email{"email": "jeevakghosh@gmail.com"}
    - slot{"email": "jeevakghosh@gmail.com"}
    - action_send_email
    - reset_slots
    - utter_goodbye
    - action_restart_conversation
