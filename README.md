# Text-sentiments-analysis
# A Python script that analyzes the sentiment of text using natural language processing (NLP) techniques. This script uses the TextBlob library to perform sentiment analysis on a given text.

from textblob import TextBlob

def analyze_sentiment(text):
    analysis = TextBlob(text)
    if analysis.sentiment.polarity > 0:
        return "Positive"
    elif analysis.sentiment.polarity == 0:
        return "Neutral"
    else:
        return "Negative"

if __name__ == "__main__":
    text = input("Enter the text to analyze: ")
    sentiment = analyze_sentiment(text)
    print(f"Sentiment of the text: {sentiment}")
    
