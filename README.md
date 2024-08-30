**Web Scraping and Data Insertion into MySQL Database**

**Description**
This project involves scraping data from a Wikipedia page listing the largest companies in the United States by revenue. The scraped data is then stored in a MySQL database. The project is divided into three main parts:

Web Scraping: Using the requests library to fetch the web page and BeautifulSoup to parse the HTML content and extract the relevant data.
Data Processing: Organizing the extracted data into a pandas DataFrame for easy manipulation and storage.
Data Insertion into MySQL: Connecting to a MySQL database, creating a table (if it doesn't exist), and inserting the scraped data into the table.

**Requirements**
Python 3.x
Libraries:
requests
beautifulsoup4
pandas
mysql-connector-python
MySQL Database

**Setup and Installation**

Clone the repository:
git clone https://github.com/RaksithSivakumar/Web-Scraping.git

cd web-scraping-mysql

Install the required Python libraries:
pip install requests beautifulsoup4 pandas mysql-connector-python

**Set up your MySQL Database:**
Install MySQL and create a database named companies_db.
Update the MySQL connection details in the script if necessary (e.g., host, user, password).

Running the Script

Run the script:
python scrape_and_store.py

This will:
Fetch the data from the Wikipedia page.
Parse and organize the data into a pandas DataFrame.
Connect to the MySQL database and create the largest_companies table if it doesn't already exist.
Insert the data into the largest_companies table.

**MySQL Table Structure**

The table largest_companies will have the following structure:

rank (INT): The rank of the company by revenue.
name (VARCHAR(255)): The name of the company.
industry (VARCHAR(255)): The industry the company operates in.
revenue (FLOAT): The revenue of the company (in billions).
employees (INT): The number of employees.
headquarters (VARCHAR(255)): The location of the company's headquarters.

**Example Output**

After running the script, the MySQL table will be populated with data that looks like this:
rank	name	industry	revenue	employees	headquarters
1	Walmart	Retail	523.96	2200000	Bentonville, AR
2	Amazon.com	Technology	280.52	798000	Seattle, WA
...	...	...	...	...	...
Error Handling

The script includes error handling to:
Capture and report MySQL connection issues.
Ensure the MySQL connection is properly closed after execution.
Future Improvements
Dynamic Data Extraction: Improve the script to handle different table structures or other types of data on the webpage.
Advanced Error Handling: Implement more robust error handling for edge cases, such as network issues during web scraping.
Data Updates: Create a scheduled task or cron job to periodically update the database with the latest data from the website.
License
This project is licensed under the MIT License. Feel free to use and modify the code for your own projects.

**Author**
Raksith
Email: your: risivandev@gmail.com
GitHub: https://github.com/RaksithSivakumar

**Acknowledgements**
Thanks to Wikipedia for providing the data.
Thanks to the open-source community for the libraries used in this project.
