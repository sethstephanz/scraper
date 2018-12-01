# scraper
    import bs4
    import requests

    url = "https://en.wikipedia.org/wiki/Chess_prodigy"
    response = requests.get(url)
    html = response.content
    print(html)

second version:

    input = input("What URL would you like to scrape? (Make sure this website it open to scraping!) ")
    input = str(input)
    
    import bs4
    import requests
    website_url = requests.get(input).text

    from bs4 import BeautifulSoup
    soup = BeautifulSoup(website_url, "html.parser")
    print(soup.prettify())
    
second version with documentation:

    #prompts user for input URL
    input = input("What URL would you like to scrape? (Make sure this website it open to scraping!) ")
    #stringifies input
    input = str(input)

    #imports bs4 module
    import bs4
    #imports requests module
    import requests
    #retrieves contents of website using requests.get() in plaintext form using .text
    website_url = requests.get("https://en.wikipedia.org/wiki/Chess_prodigy").text

    #from module bs4, we import BeautifulSoup
    from bs4 import BeautifulSoup
    #sets variable soup to results of BeautifulSoup(x, "y"), x being variable defined above
    soup = BeautifulSoup(website_url, "html.parser")
    #prints results in readable manner using BeautifulSoup's .prettify() feature
    print(soup.prettify())
