# My-First-Chatbot-in-making 
(Chatbot using NLTK & Keras)

Hey Siri, What’s the meaning of Life?

As per all the evidence, it’s chocolate for you.

Soon as I heard this reply from Siri, I knew I found a perfect partner to savour my hours of solitude. From stupid questions to some pretty serious advice, Siri has been always there for me.

How amazing it is to tell someone everything and anything and not being judged at all. A top class feeling it is and that’s what the beauty of a chatbot is.

# So, what's a chatbot? Peeps.....
A chatbot is an intelligent piece of software that is capable of communicating and performing actions similar to a human. Chatbots are used a lot in customer interaction, marketing on social network sites and instantly messaging the client. There are two basic types of chatbot models based on how they are built; Retrieval based and Generative based models.

# 1. Retrieval based Chatbots 

It uses predefined input patterns and responses. It then uses some type of heuristic approach to select the appropriate response. It is widely used in the industry to make goal-oriented chatbots where we can customize the tone and flow of the chatbot to drive our customers with the best experience.

# 2. Generative based Chatbots 

They are not based on some predefined responses.

They are based on seq 2 seq neural networks. It is the same idea as machine translation. In machine translation, we translate the source code from one language to another language but here, we are going to transform input into an output. It needs a large amount of data and it is based on Deep Neural networks.

Okay, let's deepdive into chatbot project now!

In this Python project with source code, we are going to build a chatbot using deep learning techniques. The chatbot will be trained on the dataset which contains categories (intents), pattern and responses. We use a special recurrent neural network (LSTM) to classify which category the user’s message belongs to and then we will give a random response from the list of responses.

Let’s create a retrieval based chatbot using NLTK, Keras, Python, etc.

You can download Chatbot Code & Dataset
The dataset we will be using is ‘intents.json’. This is a JSON file that contains the patterns we need to find and the responses we want to return to the user.

Please download python chatbot code & dataset from the following link: https://data-flair.training/blogs/download-python-chatbot-data-project-source-code/


# Prerequisites - 
we will use some helping modules which you can download using the python-pip command.
pip install tensorflow, keras, pickle, nltk


# How to Make Chatbot in Python?

Now we are going to build the chatbot using Python but first, let us see the file structure and the type of files we will be creating:


**Intents.json** – The data file which has predefined patterns and responses.
**train_chatbot.py** – In this Python file, we wrote a script to build the model and train our chatbot.
**Words.pkl** – This is a pickle file in which we store the words Python object that contains a list of our vocabulary.
**Classes.pkl** – The classes pickle file contains the list of categories.
**Chatbot_model.h5** – This is the trained model that contains information about the model and has weights of the neurons.
**Chatgui.py** – This is the Python script in which we implemented GUI for our chatbot. Users can easily interact with the bot.


Here are the 5 steps to create a chatbot in Python from scratch:

Import and load the data file
Preprocess data
Create training and testing data
Build the model
Predict the response






# 1. Import and load the data file

First, make a file name as train_chatbot.py. We import the necessary packages for our chatbot and initialize the variables we will use in our Python project.

The data file is in JSON format so we used the json package to parse the JSON file into Python.

# 2. Preprocess data
When working with text data, we need to perform various preprocessing on the data before we make a machine learning or a deep learning model. Based on the requirements we need to apply various operations to preprocess the data.

Tokenizing is the most basic and first thing you can do on text data. Tokenizing is the process of breaking the whole text into small parts like words.

Here we iterate through the patterns and tokenize the sentence using nltk.word_tokenize() function and append each word in the words list. We also create a list of classes for our tags.

And then we lemmatize each word and remove duplicate words from the list. Lemmatizing is the process of converting a word into its lemma form and then creating a pickle file to store the Python objects which we will use while predicting.



# 3. Create training and testing data

Now, we will create the training data in which we will provide the input and the output. Our input will be the pattern and output will be the class our input pattern belongs to. But the computer doesn’t understand text so we will convert text into numbers.



# 4. Build the model

We have our training data ready, now we will build a deep neural network that has 3 layers. We use the Keras sequential API for this. After training the model for 200 epochs, we achieved 100% accuracy on our model. Let us save the model as ‘chatbot_model.h5’.


# 5. Predict the response (Graphical User Interface)


To predict the sentences and get a response from the user to let us create a new file ‘chatapp.py’.

We will load the trained model and then use a graphical user interface that will predict the response from the bot. The model will only tell us the class it belongs to, so we will implement some functions which will identify the class and then retrieve us a random response from the list of responses.

Again we import the necessary packages and load the ‘words.pkl’ and ‘classes.pkl’ pickle files which we have created when we trained our model


Now we will develop a graphical user interface. Let’s use Tkinter library which is shipped with tons of useful libraries for GUI. We will take the input message from the user and then use the helper functions we have created to get the response from the bot and display it on the GUI.




# 6. Run the chatbot

To run the chatbot, we have two main files; train_chatbot.py and chatapp.py.


The program will open up a GUI window within a few seconds. With the GUI you can easily chat with the bot!!!





