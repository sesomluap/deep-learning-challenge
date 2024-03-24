# deep-learning-challenge
For this part of the assignment, you’ll write a report on the performance of the deep learning model you created for Alphabet Soup.

The report should contain the following:

Overview of the analysis:
* I created a model that uses information on organizations that have received funding from AlphabetSoup in the past to predict the success of future applicants, and thus more efficiently distribute AlphabetSoup's funds.
* I used the TensorFlow module to create a neural network for my model.

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?
* IS_SUCCESSFUL—Was the money used effectively
  
What variable(s) are the features for your model?
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special considerations for application
* ASK_AMT—Funding amount requested
  
What variable(s) should be removed from the input data because they are neither targets nor features?
* EIN and NAME—Identification columns

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

I ended up going with three hidden layers totaling 140 neurons and two activation functions, after playing with a number of different configurations. 
It felt like no matter what I did, I was hard capped around 73% accuracy.
My final model was my most accurate, but only fractions of a percent more accurate than a one hidden layer 10 neuron model.

Were you able to achieve the target model performance?

no, I ended up around 73%

What steps did you take in your attempts to increase model performance?

I played with the number of layers, the number of neurons, the activation function types, and the number of epochs.
Usually the model's performance stabilized within 2 or 3 epochs, so there was little functional difference between running 20 and 100.
More intricate models did generally perform better, but the gains were so marginal as to not be worth the extra computation power.

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Every attempt I ran at a deep learning model ended up at more or less 73% performance and 55% loss.
This model would represent a significant improvement on our historic donation success rate of 53%.
There are two things we could do to improve our neural network model: run kerastuner to optimize the model itself, or clean outliers from the data to see if that improves predictive power.
It might benefit us to run a RandomForest or other supervised learning model, so we can see which of the application categories are most predictive of future success.
