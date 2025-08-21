Link to video presentation for web scrapping: https://drive.google.com/drive/folders/1rOg4PJ2nhY-mHXl-Ln3WUz_4Doq8lwAN?usp=drive_link

This lesson helps us to understand how to scrap a website in Python using BeautifulSoup. For the purpose of learning, I scrapped the website: List of The Largest Companies in The United State by Revenue

Scraping a website using BeautifulSoup in Python involves several steps: Install Libraries.
 
Install requests for fetching HTML and beautifulsoup4 for parsing.
 
Code
 
    pip install requests beautifulsoup4
Import Libraries.
 
Import requests and BeautifulSoup into your Python script.
 
Python
 
    import requests
    from bs4 import BeautifulSoup
Fetch HTML Content.
 
Send an HTTP GET request to the target URL using requests.get() and retrieve the HTML content using .text.
 
Python
 
    url = "https://example.com"  # Replace with the target URL
    response = requests.get(url)
    html_content = response.text
Parse HTML with BeautifulSoup.
 
Create a BeautifulSoup object by passing the HTML content and specifying a parser (e.g., 'html.parser').
 
Python
 
    soup = BeautifulSoup(html_content, 'html.parser')
extract desired information.
 
Use BeautifulSoup's methods to navigate and extract data from the parsed HTML.
 
soup.find('tag_name'): Finds the first occurrence of a tag.
soup.find_all('tag_name'): Finds all occurrences of a tag.
You can refine your search by specifying attributes like class_, id, or other attributes.
element.get_text(): Extracts the text content of an element.
element['attribute_name']: Accesses the value of an attribute.
Recommendations When Using BeautifulSoup

Rate Limiting: Introduce delays between requests to avoid overwhelming the server.
 
User Agents & Proxies: Rotate user agents or use proxy servers to mimic different browsers or locations.
 
Error Handling: Implement try-except blocks to handle potential network errors or malformed HTML.
Kindly click on the above link to see how I was able to scrap the website (List of The Largest Companies in The United State)
