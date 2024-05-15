**Sentiment Analysis on Product Reviews**


This repository contains a Python project for sentiment analysis on product reviews. The script loads a dataset of product reviews, preprocesses the text, analyzes the sentiment of the reviews, and saves the results to a file.

**collections**
json

nltk (for stopwords)

Install the required libraries using pip:

bash

Copy code

pip install nltk

Usage
Load the dataset: Ensure that your dataset file record.json is in the same directory as the script. The dataset should be in JSON format.
Run the script: Execute the script to preprocess the data and perform sentiment analysis.

bash
Copy code

python main.py

View results: The results of the sentiment analysis will be saved in results.txt.
Project Structure

main.ipynb: Jupyter notebook containing the main code.

record.json: JSON file containing the product reviews dataset.

stopwords.txt: Text file containing the list of stopwords to be removed during preprocessing.

result.txt: Output file where the sentiment analysis results are saved.

**Code Explanation**
Data Loading

The dataset is loaded from a JSON file:

python

Copy code

record = [json.loads(line) for line in open('record.json')]


Data Preprocessing:

Unnecessary columns are removed, and text is cleaned by converting to lowercase, removing punctuation, and eliminating stopwords.


Sentiment Analysis:

The reviews are categorized into positive, negative, and neutral based on their ratings. The most common words in positive and negative reviews are identified.


Sentiment Scoring:

A sentiment score is calculated for each review based on predefined word weights, and the reviews are classified as positive, negative, or neutral.



output:
The results, including the sentiment scores and classifications for the first and last five reviews, are written to result.txt.

python
Copy code

with open("result.txt", "w") as file:

    file.write("Result:\n\n")
    
    # Write sentiment analysis results here
