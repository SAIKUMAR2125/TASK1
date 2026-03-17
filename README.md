# TASK1
TASK1 GITHUB
import requests
from bs4 import BeautifulSoup

# URL of the website to scrape
url = "https://quotes.toscrape.com"

# Send request to the website
response = requests.get(url)

# Parse the HTML content
soup = BeautifulSoup(response.text, "html.parser")

# Find all quotes
quotes = soup.find_all("span", class_="text")

# Print quotes
for i, quote in enumerate(quotes, 1):
    print(f"{i}. {quote.text}")
