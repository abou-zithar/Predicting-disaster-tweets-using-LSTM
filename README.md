# Natural Language Processing (NLP) for Tweet Classification

This project involves a series of steps to build and train a machine learning model to classify tweets as related to a real disaster or not. The project uses the TensorFlow library for deep learning and NLP preprocessing techniques to achieve the classification task.



<h2> Requirements</h2>

- Load the dataset
- Check head and info of the data
- Is there a missing data [how many and the precentage if there]?
- How many data in each class?
- Get the top 15 locations of the data
- Get the top 15 keyword in the data
- What are the most common words?
- What are the most common stop words?
- Use nlp to prepare dataset [tokenization, pad sequence, etc.]
- Prepare train, test sets
- Train your LSTM structure
- Evaluate the model and make predictions
- Save your model
- Post your project into GitHub
<hr>
<h2> Columns Description</h2>

- id ===> a unique identifier for each tweet
- text ===> the text of the tweet
- location ===> the location the tweet was sent from (may be blank)
- keyword ===> a particular keyword from the tweet (may be blank)
- target ===> in train.csv only, this denotes whether a tweet is about a real disaster (1) or not (0)

<hr>

## Prerequisites

Before running the code, make sure to have the following libraries installed:

- `pandas`: Install using `pip install pandas`
- `tensorflow`: Install using `pip install tensorflow`
- `numpy`: Install using `pip install numpy`
- `matplotlib`: Install using `pip install matplotlib`
- `seaborn`: Install using `pip install seaborn`
- `nltk`: Install using `pip install nltk`

Additionally, you need to have access to the necessary dataset files (`train.csv` and `test.csv`) from your Google Drive.

## Data Loading and Exploration

- The dataset consists of tweet data with features such as `id`, `text`, `location`, `keyword`, and `target`.
- The data is loaded using Pandas and its structure is explored using the `.head()` and `.info()` functions.

## Data Preprocessing

- Missing data is observed in the `keyword` and `location` columns.
- Data is divided into two classes: disaster (1) and non-disaster (0).
- The most common words and stop words in the text data are analyzed.

## NLP Preprocessing

- The tweets are cleaned to remove mentions, links, numbers, and symbols using regular expressions.
- The text data is tokenized and then padded to ensure uniform length.

## Model Building

- A sequential model is created using TensorFlow, consisting of an embedding layer, LSTM layer, and dense layers.
- The model is compiled using the RMSprop optimizer and binary cross-entropy loss.
- The model is trained using the training data and validated using validation data.

## Model Evaluation

- The training history is plotted to visualize the loss and accuracy during training.
- The model's performance is evaluated using the validation dataset.
- The model's predictions are obtained for the test dataset.

## Post-processing and Output

- Predictions are converted into binary (0 or 1) based on a threshold.
- The test dataset's predictions are organized into a DataFrame with the corresponding `id` and `target` columns.
- The DataFrame is saved as a CSV file named `output.csv`.

## Save Model

- The trained model is saved in an `.h5` file using TensorFlow's model saving mechanism.

## Note

- The project assumes that you have the necessary dataset files (`train.csv` and `test.csv`) available in your Google Drive.
- Adjust the paths to the dataset files and output file as needed based on your directory structure.

## Author

Created by [Your Name]

## License

This project is licensed under the [MIT License](LICENSE).













