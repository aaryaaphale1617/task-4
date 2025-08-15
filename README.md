This script is a basic web scraper built with requests and BeautifulSoup that:

Sends a GET request to http://books.toscrape.com/catalogue/page-1.html using the requests library.

Checks HTTP status code — if 200 OK, it processes the HTML; otherwise, it prints an error message.

Parses the HTML using BeautifulSoup to find each book’s container (.product_pod).

Extracts data for each book:

Title — from the title attribute of the <a> tag inside <h3>.

Price — from the .price_color element.

Rating — from the second CSS class of the <p> tag containing the star rating.

Availability — from .availability, stripped of whitespace.

Link — from the href attribute of the book title link.

Stores extracted data in a list of dictionaries (books).

Prints the results in a readable format, prefixing links with the base URL.

Final outcome: The code retrieves and displays all books listed on page 1 of the Books to Scrape website with their title, price, rating, stock availability, and direct link.
