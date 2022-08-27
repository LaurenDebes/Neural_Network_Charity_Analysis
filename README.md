# Neural Network Charity Analysis
We are tasked with helping a foundation create a binary classifier capable of predicting whether applicants will be successful if funded by Alphabet Soup. We will be using a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. First we will preprocess the data, then compile/train/evaluate the model, then attempt to optimize the model for even better results.

## Results

### Data preprocessing:
  - <b>Target:</b> The target for our code is the IS_SUCCESSFUL column. It is binary and answers if the money used effectively
  - <b>Features:</b> Our features are each of the variables except for IS_SUCCESSFUL and the ID columns (EIN and NAME)
  - <b>Unnecessary Variables:</b> ID Columns (EIN and NAME)

### Compiling, Training, and Evaluating the Model:
  - <b>Number of Neurons:</b> Deep learning models use a single neuron across multiple layers. We have used two layers. We attempted to use more later on to compare and it did not lead to better scores. The activation function relu for our hidden layers is relu and sigmoid for the output layer. Relu will allow us to recieve any output value form 0-infinity, and all negative values are just zero. With such a large data set, it is a good activation function for our hidden layers. For our output layer, we have used sigmoid which transforms the output to between 0-1.
  - <b>Model Performance:</b> The model was put through 4 attempts at optimization, but the target model performance (accuracy of over 75%) was unable to be reached.
  ![results.png](https://raw.githubusercontent.com/LaurenDebes/Neural_Network_Charity_Analysis/main/results.png)
  - <b>Attempts to increase model performance:</b> 
    - Attempt 1: First, I removed the column ASK_AMT as it had 8,747 unique values that I thought may be confusing/over complicating the model. The results were generally the same, still 73% accuracy score.
    - Attempt 2: Then, I doubled the number of number of nodes in the hidden layers. Again, this resulted in generally the same results.
    - Attempt 3: Next, I added another hidden layer with 11 nodes (proportional to the difference between the first two layers). Again, generally the same results.
    - Attempt 4: Lastly, I tried out all the types of activation functions on the hidden layers and output layer. Each attempt only lowered the accuracy score.

## Summary
The final results are at 73% accuracy. I would consider another learning model for a higher score. I would attempt to use Random Forest classifier instead because it also has high accuracy but combines multiple smaller models to a more robust and accurate model. We are only working with tabular data so it would still be appropriate. More neurons may be helpful.
