# scraper
    import bs4
    import requests

    url = "https://en.wikipedia.org/wiki/Chess_prodigy"
    response = requests.get(url)
    html = response.content
    print(html)

second version (using prettify):

    import bs4
    import requests
    website_url = requests.get("https://en.wikipedia.org/wiki/Chess_prodigy").text

    from bs4 import BeautifulSoup
    soup = BeautifulSoup(website_url, "html.parser")
    print(soup.prettify())
