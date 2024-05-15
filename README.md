<H3>NAME : S.LOKESH SAI DILEEP</H3>
<H3>REG NO: 212221230111</H3>
<H3>DATE:15/05/2024</H3>
<H1 Align="center">Project Based Experiment<H1>
  
### Objective:
Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.
<H3>Program:</H3>

```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)

```
<H3>Output:</H3>

![image](https://github.com/22002102/Project-Based-Experiment-AAI/assets/119091638/a6539c89-7efd-4679-b2d3-b7da9feb4393)

![image](https://github.com/22002102/Project-Based-Experiment-AAI/assets/119091638/fd6249e6-f2ad-48e9-b3a9-13f9747c94ca)

<H3>Inference:</H3>
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only negative feedback for the code is done.
