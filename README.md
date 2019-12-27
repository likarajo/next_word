# Text Generation

Deep Learning model to predict the next words based on a sequence of input words.  

## Dependencies

* Nltk
* Tensorflow
* Keras
* Numpy
* Pickle

<br>

`pip install -r requirements.txt`  

## Data

The data consists of collected text related to the space, including the universe and the solar system.  

## Data Preprocessing

* Remove punctuations and numbers
* Remove single characters
* Replace multiple spaces with a sinlge space
* Convert text to lowercase

## Vectorize words

Deep learning models are based on statistical algorithms. Hence, in order to work with deep learning models, we need to convert words to numbers.  

* Tokenize the text into individual words
* Remove stopwords (optional): application specific
* Convert the tokenized words to numbers
* Create word-to-index dictionary
* Create index-to-word dictionary (by reversing)

## Text generation: Many-to-One Sequence problem

* Input is a sequence of words
* Output is a single word

### Long Short Term Memory (LSTM) model

* Recurrent Neural Network (RNN)
* Accepts data in 3D format
  * number of samples
  * number of time-steps
  * features per time-step
* Outputs data in 2D format
  * number of samples
  * number of unique words in the corpus

### Building and training the model

* Modify the shape of input sequences and the corresponding outputs
* Normalize the input
* Create Stacked LSTM Sequential model
* Train the model

### Make predictions

* Randomly select a sequence
* Obtain the words from index-to-word dictionary
* Predict a one-hot encoded array of indices
  * the index that contains 1 will be the index value of the next word

## Improvements

* Change model hyperparameters
  * number of neurons in LSTM layers
  * number of LSTM layers
  * number of epochs
* Remove the stop words from the training set
  * This will generate words other than stop words in the test set also. Hence it depends on the type of application).  
* Create a character-level text generation model that predicts the next N characters.  