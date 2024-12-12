
# Lite-Side Vader: Vanilla Python Sentiment Analysis
```python
###############
# Sample Use 1
###############
analyzer = SentimentIntensityAnalyzer()
text = "This sentiment is absolutely amazing!"
scores = analyzer.polarity_scores(text)

###############
# Sample Use 2
###############
python liteside_vader.py "This deal is getting worse all the time"
```

liteside_vader_vanillapython_sentiment_analysis

## Original (I think) (Legendary) Vader NLP project:
MIT license Vader: https://github.com/cjhutto/vaderSentiment 



This Vanilla Python Lite-Side Vader was inspired by 
the fact that NLTK version is (or was at the time 
of writing) bloated, 3rd party dependent, 
and not working. See code the doesn't (or didn't)
 run at this URL:
https://www.nltk.org/_modules/nltk/sentiment/vader.html
The incomplete code did not run because it was 
missing this code section (or maybe they could not 
keep up with the dependency chains in their evolving code)
```python
import nltk
nltk.download('vader_lexicon')
```
Relying upon dependencies is an endless liability.

Vader, as you can see here, is lite, fast, and beautiful,
and does not need an empire of supply chains.


This lite-side vanilla python version code 
does not require any installed 3rd party 
libraries, packages, or other dependencies.
It uses only standard-library python and
(as of python 3.12, should run out of the box):
```python
python liteside_vader.py "This deal is getting worse all the time"
```

You will need the (included) lexicon file,
which you can also make/get by running this:
```python
import json
import nltk
nltk.download('vader_lexicon')

# Run this once to create the JSON file
def create_json_lexicon():
    lexicon_file = nltk.data.load("sentiment/vader_lexicon.zip/vader_lexicon/vader_lexicon.txt")
    lex_dict = {}
    
    for line in lexicon_file.split("\n"):
        if line.strip():  # Check if line is not empty
            (word, measure) = line.strip().split("\t")[0:2]
            lex_dict[word] = float(measure)

    print("dict len is 7502? -> ", len(lex_dict))
    
    # Save to JSON file
    with open('vader_lexicon.json', 'w', encoding='utf-8') as f:
        json.dump(lex_dict, f, ensure_ascii=False, indent=2)

# Run this function once to create the JSON file
create_json_lexicon()
```

Is this.. 
https://github.com/ckw017/vader-sentiment-rust
a new hope? >*<
