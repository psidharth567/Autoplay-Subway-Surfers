# Autoplay-Subway-Surfers
This repository can be used to train a 3D ViT which can be used to autoplay Subway Surfers.

# Data Collection
Data can be colected using Data_collection.py. Just run the script and play Subway Surfers and the script will start capturing screen and assign labels. 
Play for about 10 hours to get enough data. The more data, the better the model.

# Training the model
Train the model using main.py
It uses 3D ViT. It takes in input of 3 frames of the game and predicts the action needed to be taken. There are 5 actions that the model can take: "LEFT","RIGHT","UP","DOWN","NOTHING"

A key issue in Subway Surfers is that the speed of the game keeps increasing as time progresses. The moment at which actions must be carried out changes based on the speed of the game (the speed at which the character is running). 
The model takes in 3 frames each seperated by an interval. Based on the temporal sequence of 3 frames, the model will hopefully deduce the speed at which the game is running and can take actions accordingly.

