# Python Blog Scraper (BeautifulSoup)
A Python script that scrapes blog titles and publication dates from Pixelford’s blog using BeautifulSoup and Requests. It extracts blog titles, formats their publish dates, and prints everything in a clean readable format.
# Features
- Scrapes blog titles automatically
- Extracts publish dates from article metadata
- Formats dates into human-readable text
- Uses a randomized user-agent header
- Lightweight and fast
# User-Agent Handling
This project uses a randomized User-Agent header when making HTTP requests:
    headers = {'User-Agent': str(random_number)}
This is done to reduce the chance of the request being blocked by basic anti-scraping systems, which may deny requests from unknown or default Python identifiers.
Some websites block scripted requests unless they resemble a browser request.  
Randomizing the header helps prevent simple request filtering.
Note: This is a lightweight workaround intended for learning purposes, not a production-grade scraping solution.
# Requirements
- Python 3.x
- requests
- beautifulsoup4
# How It Works
1. Sends HTTP request to the blog with randomized user-agent
2. Collects HTML content from the page
3. Parses HTML with BeautifulSoup
4. Finds every blog `<article>`
5. Extracts title and publish date
6. Formats the date for readability
7. Prints results line-by-line
