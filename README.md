🕸️ Quotes Web Scraper

A simple Python web scraping project that extracts quotes, their authors, and associated tags from Quotes to Scrape. The extracted information is organized into a Pandas DataFrame and exported to a CSV file for further analysis.

✨ Features
🌐 Website Scraping: Fetches HTML content from the Quotes to Scrape website.
💬 Quote Extraction: Collects quotes displayed on the webpage.
✍️ Author Extraction: Retrieves the name of each quote's author.
🏷️ Tag Extraction: Collects tags associated with each quote.
📊 Data Organization: Stores the extracted information in a Pandas DataFrame.
📁 CSV Export: Saves the scraped data into quotes.csv.
⚠️ Error Handling: Checks the HTTP response status and raises an exception if the request fails.
⏱️ Request Timeout: Uses a 10-second timeout to avoid waiting indefinitely for a response.
🛠️ Technologies Used
Python – Core programming language.
Requests – Sends HTTP requests to retrieve webpage content.
BeautifulSoup4 – Parses HTML and extracts relevant information.
Pandas – Organizes scraped data into a DataFrame and exports it to CSV.
📂 Project Structure
quotes-web-scraper/
│
├── main.py
├── requirements.txt
├── quotes.csv
└── README.md

main.py – Contains the web scraping code.
requirements.txt – Lists the required Python libraries.
quotes.csv – Generated file containing the scraped quotes.
README.md – Project documentation.

Note: The quotes.csv file is automatically created when the script runs successfully, so you do not need to create it manually.

⚙️ Installation and Setup
1. Clone the Repository
git clone <your-repository-url>
cd quotes-web-scraper


Replace <your-repository-url> with your actual Git repository URL.

2. Create a Virtual Environment (Optional)
python -m venv venv


Activate the environment:

Windows

venv\Scripts\activate


Linux / macOS

source venv/bin/activate

3. Install Dependencies

Create a requirements.txt file containing:

requests
beautifulsoup4
pandas


Install the required packages:

pip install -r requirements.txt

4. Run the Script

Save your Python code as main.py and execute:

python main.py


The script will retrieve the webpage, extract quotes and related information, display the data in the terminal, and save the results to quotes.csv.

🚀 How It Works
Send HTTP Request: Uses requests.get() to retrieve the webpage with a 10-second timeout.
Check Response: Prints the HTTP status code and calls raise_for_status() to detect unsuccessful HTTP responses.
Parse HTML: Uses BeautifulSoup with the built-in html.parser.
Extract Quotes: Finds HTML elements containing quotes.
Extract Authors: Retrieves the author associated with each quote.
Extract Tags: Collects all tags associated with each quote and joins them into a comma-separated string.
Create DataFrame: Stores the extracted records in a Pandas DataFrame.
Export to CSV: Saves the data to quotes.csv without including the DataFrame index.
💻 Example Output

The terminal displays the HTTP status code and a DataFrame similar to the following:

Status Code: 200

                                               Quote          Author                         Tags
0  “The world as we have created it is a process...  Albert Einstein  change, deep-thoughts, thinking...
1  “It is our choices, Harry, that show what we...    J.K. Rowling    abilities, choices
2  “There are only two ways to live your life...     Albert Einstein  inspirational, life, live


The sample rows above are illustrative; the exact output depends on the website's current content.

After the data is processed, the script prints:

Data saved successfully to quotes.csv

📊 Output CSV Format

The generated quotes.csv file contains three columns:

Column	Description
Quote	The text of the quote.
Author	The name of the author.
Tags	Comma-separated tags associated with the quote.

Example CSV structure:

Quote,Author,Tags
"Example quote text",Example Author,"inspiration, life"

📦 Requirements
Python 3.9 or a compatible Python version.
An active internet connection.
Required Python libraries: requests, beautifulsoup4, and pandas.
Access to the target website.
⚠️ Important Notes
The script currently scrapes only the quotes displayed on the website's first page.
The request timeout is set to 10 seconds.
If the website returns an unsuccessful HTTP status code, raise_for_status() raises an exception.
Website HTML changes may require updating the element selectors.
Always respect the target website's terms of use and scraping policies. This project uses a website intended for practicing web scraping.
🔮 Future Enhancements
Scrape quotes from all available pages using pagination.
Add retry logic for temporary network errors.
Export the data to Excel or JSON.
Filter quotes by author or tag.
Add duplicate detection and data cleaning.
Build a user interface using Streamlit.
Add logging to track scraping progress and errors.
👨‍💻 Author

Developed as a Python project to demonstrate web scraping, HTML parsing, data extraction,
