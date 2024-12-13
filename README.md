
# Lite-Side Vader: Vanilla Python Sentiment Analysis
liteside_vader_vanillapython_sentiment_analysis

## How to Use vader_lite.py:
### Method 1. Use as bash script for string 
(vanilla python, no env needed) 
```bash
### python vader_lite.py "YOUR INPUT IN QUOTES"
``` 

### Method 2. Use as bash script for text-file-path 
(vanilla python, no env needed) 
```bash
python vader_lite.py -p <text_file_path>
``` 
e.g.
```bash
python vader_lite.py -p "This deal is getting worse all the time."
``` 

### Method 2. Within python, import class, 
call class methods on input
```python
from vader_lite import SentimentIntensityAnalyzer  # import from local module
analyzer = SentimentIntensityAnalyzer()  # instance of class
input_text = "This sentiment is absolutely amazing!"
scores = analyzer.polarity_scores(input_text)  # call a 'class-method' (a function)
print(scores)
```



### Current version is self contained with a built-in lexicon.
But in the archive you can find the lexicon file and a version that imports that file.

## Original (I think) (Legendary) Vader NLP project:
MIT license Vader: https://github.com/cjhutto/vaderSentiment 

This lite-side vanilla python version of Vader code 
uses only standard-library python and
(as of python 3.12, should run out of the box).

This lite-side vanilla python version of Vader code 
does not require any installed 3rd party 
libraries, packages, or other dependencies.

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
and does not need an empire of supply chain items to work.


Is this...
https://github.com/ckw017/vader-sentiment-rust
 ...a new hope? >*<
