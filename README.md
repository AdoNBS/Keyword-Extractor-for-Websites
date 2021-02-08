# Keyword-Extractor-for-Websites

A tool for Extracting keywords from given attributes of a particular website

# Keyword Extractor: A Smart, Automatic, Fast and Lightweight Keyword Extractor with Deep Learning Application with Python

![img](https://github.com/elvinaqa/Keyword-Extractor-for-Websites/blob/main/images/1_nHfayfdmxAApbg84iMrJqQ.gif)

This project is made for keyword extraction of the semantically similar words from websites and their meta data. Can be used in SEO, marketing and few other related applications. 
It gets a url or the html content of a web page and a list of sample data which we want to scrape from that page. **This data can be text, url or any html tag value of that page.**

## Installation

It's compatible with python 3.

- Install latest version from git repository using pip:
```bash
$ pip install git+https://github.com/elvinaqa/Keyword-Extractor-for-Websites.git

```
Also 
```
$ pip install -r requirements.txt 
```

## How to use

## How it seems?
![img](https://github.com/elvinaqa/Keyword-Extractor-for-Websites/blob/main/images/text.PNG)
![img](https://github.com/elvinaqa/Keyword-Extractor-for-Websites/blob/main/images/col.PNG)
### Results
![img](https://github.com/elvinaqa/Keyword-Extractor-for-Websites/blob/main/images/2nd%20oage.PNG)

```python
from autoscraper import AutoScraper

url = 'https://stackoverflow.com/questions/2081586/web-scraping-with-python'

# We can add one or multiple candidates here.
# You can also put urls here to retrieve urls.
wanted_list = ["What are metaclasses in Python?"]

scraper = AutoScraper()
result = scraper.build(url, wanted_list)
print(result)
```

Here's the output:
```python
[
    'How do I merge two dictionaries in a single expression in Python (taking union of dictionaries)?', 
    'How to call an external command?', 
    'What are metaclasses in Python?', 
    'Does Python have a ternary conditional operator?', 
    'How do you remove duplicates from a list whilst preserving order?', 
    'Convert bytes to a string', 
    'How to get line count of a large file cheaply in Python?', 
    "Does Python have a string 'contains' substring method?", 
    'Why is “1000000000000000 in range(1000000000000001)” so fast in Python 3?'
]
```
Now you can use the `scraper` object to get related topics of any stackoverflow page:
```python
scraper.get_result_similar('https://stackoverflow.com/questions/606191/convert-bytes-to-a-string')
```


**You may want to get other info as well.** For example if you want to get market cap too, you can just append it to the wanted list. By using the `get_result_exact` method, it will retrieve the data as the same exact order in the wanted list.

**Another example:** Say we want to scrape the about text, number of stars and the link to issues of Github repo pages:

```python
from autoscraper import AutoScraper

url = 'https://github.com/alirezamika/autoscraper'

wanted_list = ['A Smart, Automatic, Fast and Lightweight Web Scraper for Python', '2.5k', 'https://github.com/alirezamika/autoscraper/issues']

scraper = AutoScraper()
scraper.build(url, wanted_list)
```

Simple, right?

```

## Tutorials

- See [this gist](https://gist.github.com/alirezamika/72083221891eecd991bbc0a2a2467673) for more advanced usages.
- [AutoScraper and Flask: Create an API From Any Website in Less Than 5 Minutes](https://medium.com/better-programming/autoscraper-and-flask-create-an-api-from-any-website-in-less-than-5-minutes-3f0f176fc4a3)

## Issues
Feel free to open an issue if you have any problem using the module.


## Support the project

<a href="https://ko-fi.com/eapresents" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-black.png" alt="Buy Me A Coffee" height="45" width="163" ></a>


#### Happy Coding  ♥️
