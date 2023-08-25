# GitEmo
A Google Chrome plugin to augment comments on Github with emojis, based on the sentiment of the comments posted.

This project was collaboratively developed by my classmate and me as part of the requirements for the Industrial Software Engineering course in the second semester of our M.Tech program.

It is a Google Chrome plugin designed to enhance the commenting experience on GitHub by augmenting comments with
emojis based on the sentiment expressed in the text. Leveraging sentiment analysis techniques, GitEmo accurately analyzes the sentiment of comments, classifying them in 9 categories. By mapping
specific emojis to each sentiment category, users can easily convey their emotions and add an extra layer of expression to their comments.



# DESIGN AND METHODOLOGY

To design GitEmo we used libraries and modules, including Flask,Selenium for web scraping, pandas for data manipulation, numpy,
re for regular expressions, nltk toolkit is used for preprocessing the data like removing the stopwords and converting the text into tokens, and NRCLex is the python library used for sentiment analysis.
Flask is a popular Python web framework that allows you to build web applications. It provides a simple and efficient way to handle HTTP requests, define routes, and generate HTTP responses. In
the provided code, Flask is used to create a web server that exposes an API endpoint.

# Development

Web Scraping: The script uses Selenium WebDriver to automate a web browser (Chrome) and navigate to the specified URL. It finds all elements with the class name "comment-body," which presumablyrepresents the comments on the page. It retrieves the text contentof each comment and stores it in the list.

Text Cleaning: A function is defined to clean the text extracted from comments. It performs the following steps:

1. Removes non-alphabetic characters using regular expressions.

2. Converts the text to lowercase.

3. Tokenize the text into individual words.

4. Lemmatize each word (reduces it to its base or dictionary form)
using WordNet lemmatizer.

5. Removes stopwords (common words like "the," "is," etc.) from
the text.

6. Joins the cleaned words back into a string.
Sentiment Analysis: The sentiment scores are calculated using
a function which uses the NRCLex library to perform sentiment
analysis on the cleaned text. It calculates sentiment scores for different emotion categories such as anger, anticipation, disgust, fear,
joy, positive, negative, sadness, surprise, and trust. It then maps
each sentiment category to an appropriate emoji using a predefined
dictionary.

Applying Text Processing and Sentiment Analysis: The code
iterates through each comment text and performs various steps of
analysis.

Returning the Result: The final result is a dictionary containing
the response (which should be the HTTP response from the provided URL) and the sentiment scores for each comment. The result
is returned as a JSON response.

Flask Server: Flask application creates an endpoint /process url
that accepts POST requests. It retrieves the URL from the request
payload to process the URL. It is the job of Flask to return the results
in response.



# DEMONSTRATION

Step1: Download Zip folder and extract it

Step2: Run app.py file from it

Step3: Open google chrome and load unpack the zip folder

Step4: Now open any GitHub page in Google chrome and right
click anywhere on that page(especially comments)

Step5: Click on create documentation and we will see the emojis
attached with the comments

# Note

The attached mp4 file in the repository contains a demonstration video on how to install and use the chrome extension from the files present in this repository.
