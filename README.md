# Crawler
Crawler for self-learning

爬IT標題

import requests
from bs4 import BeautifulSoup as bs
import pandas as pd

url = 'https://ithelp.ithome.com.tw/'
res = requests.get(url, verify = True)
#print(res.text)
soup = bs(res.text, 'html.parser')
a = soup.find_all(class_ = "qa-list__title-link")
for b in a:
    print(b.text)

