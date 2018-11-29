# Functionality of the code
* Chatbot to talk with user and setup an appointment with some speciality in a hospital
* The availability of the doctor is controlled by # DocAvail.csv
* This mimics the presence of a database where information is present and the input of the user can be cross checked with the data present
* Once the user enters the data, if no doctor is available the chatbot will reply back and ask the user to enter the details again
* If the doctor is available , appointment is scheduled





# Instructions for Installation

## Requirements : ubuntu system with python 3.5 installed

PWD = $HOME

## Setup Virtual environment

1. mkdir venv_chatbot 
2. virtualenv --system-site-packages -p python3 ./venv_chatbot
3. source ./venv_chatbot/bin/activate

## Install dependencies

4. pip install rasa_core
5. pip install rasa_nlu[tensorflow]
6. pip install spacy
7. python -m spacy download en_core_web_md
8. python -m spacy link en_core_web_md en
9. pip install pandas
10. pip install duckling
11. git clone https://github.com/sfrpl/chatbot
12. cd chatbot/chatroom
13. yarn install
14. yarn build

## Running the code
(in the existing terminal) - T1

15. yarn serve
### Before running 15 ensure the current working directory is $/chatbot/chatroom

## Open another terminal - T2
PWD = $HOME

16. source ./venv_chatbot/bin/activate
17. cd chatbot
18. python -m rasa_core_sdk.endpoint --actions actions
### Before running 18 ensure the current working directory is $/chatbot

## Open another terminal - T3
PWD = $HOME

19. source ./venv_chatbot/bin/activate
20. cd chatbot
21. python run_bot.py
### Before running 18 ensure the current working directory is $/chatbot

## Open another terminal - T4
22. source ./venv_chatbot/bin/activate
23. cd chatbot
24. Install docker
25. docker run -p 8000:8000 rasa/duckling


## Open browser

21. Point to http://localhost:8080
22. Chat with the bot



    

    


