# Twitter Data Scraping and Analysis

## Introduction

This repository contains a Python-based project for scraping Twitter data and analyzing it using text processing techniques. The project employs the `tweepy` library to fetch recent tweets based on specific queries and performs various text analysis tasks, including tokenization, term frequency computation, bigram frequency analysis, and the creation of a word cloud visualization.

This project is an excellent starting point for individuals interested in text mining and sentiment analysis, particularly with data obtained from Twitter. Please note that due to rate limits imposed by the Twitter API, the data collection process may take some time.

**NOTE**: To use this project, you need access to the Twitter API. Ensure you have a valid bearer token to authenticate your requests.

## Datasets Used

The data for this project is sourced directly from the Twitter API using the `tweepy` library. This allows real-time data collection based on user-defined queries. In this example, the project fetches tweets containing the hashtag `#RealMadrid` in English, excluding retweets.

The collected data is saved in a CSV file (`tweets.csv`) and includes the following fields:

- Tweet ID
- Tweet Text
- Edit History Tweet IDs (if any)

## Environment Setup

The environment details for this project are as follows:

- Python - 3.11.0
- The project is developed to run in a `.venv` virtual environment.

The following libraries are required to run this project:

- `tweepy`
- `pandas`
- `nltk`
- `wordcloud`
- `matplotlib`

## Installation

To run the code in this repository, you need to install the required dependencies. You can do this by following these steps:

1. Clone the repository to your local machine.

   ```bash
   git clone <repository-url>
   ```

2. Navigate to the project directory.

   ```bash
   cd <repository-directory>
   ```

3. Create a virtual environment using `venv`.

   ```bash
   python3 -m venv .venv
   ```

4. Activate the virtual environment.

   - On Windows:
     ```bash
     .venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source .venv/bin/activate
     ```

5. Install the required dependencies from the `requirements.txt` file.

   ```bash
   pip install -r requirements.txt
   ```

6. Set up your Twitter API bearer token.

   You can either:

   - Set it as an environment variable directly:
     ```bash
     export BEARER_TOKEN=<your-twitter-api-bearer-token>
     ```
   - Or, create a `.env` file in the project root directory and add your bearer token:
     ```
     BEARER_TOKEN=<your-twitter-api-bearer-token>
     ```

7. Run the script to fetch and analyze Twitter data.

## Steps Followed

### 1. Data Scraping

- Use the `tweepy` library to fetch recent tweets based on a predefined query.
- Save the retrieved data to a CSV file for further analysis.

### 2. Data Preprocessing

- Tokenize the text of tweets using the `nltk` library to break them into individual tokens.
- Filter out common stopwords, punctuation, and irrelevant tokens.

### 3. Text Analysis

- Compute term frequencies and identify the most common words and hashtags.
- Analyze bigram frequencies to identify common word pairs.
- Compute co-occurrence frequencies for unique terms.

### 4. Visualization

- Generate a word cloud to visualize the most frequently occurring terms in the dataset.
- Display analysis results using `matplotlib`.

## Conclusion

This project demonstrates how to integrate Twitter data scraping with text analysis techniques to gain insights from social media data. While this is a basic implementation, it serves as a strong foundation for more complex analyses, such as sentiment analysis, topic modeling, and trend prediction.

Happy coding ❤️
