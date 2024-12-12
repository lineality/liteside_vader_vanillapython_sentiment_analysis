
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
python vl3.py "This deal is getting worse all the time"  # |o|  |o|
```

liteside_vader_vanillapython_sentiment_analysis

### Version 3 Note: vl3.py is self contained with a built-in lexicon.

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
(as of python 3.12, should run out of the box).

There is a version with a standard lexicon file.
## VL3
Version 3: vl3.py has a built in lexicon dictionary and so is
better suited for production datascience and deployment.

Is this...
https://github.com/ckw017/vader-sentiment-rust
 ...a new hope? >*<
