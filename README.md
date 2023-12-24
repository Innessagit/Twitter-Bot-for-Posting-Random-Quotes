# Twitter-Bot-for-Posting-Random-Quotes
Create a basic Twitter bot to post random quotes.
import tweepy
import random

def post_random_quote():
    # Configure Twitter API credentials
    consumer_key = 'your_consumer_key'
    consumer_secret = 'your_consumer_secret'
    access_token = 'your_access_token'
    access_token_secret = 'your_access_token_secret'

    auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
    auth.set_access_token(access_token, access_token_secret)

    api = tweepy.API(auth)

    # Example list of quotes
    quotes = ["Quote 1", "Quote 2", "Quote 3"]

    # Select a random quote
    random_quote = random.choice(quotes)

    # Post the quote to Twitter
    api.update_status(status=random_quote)

post_random_quote()
