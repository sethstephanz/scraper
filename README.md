# scraper
import bs4
import requests

url = "https://en.wikipedia.org/wiki/Chess_prodigy"
response = requests.get(url)
html = response.content
print(html)
