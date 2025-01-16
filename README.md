

```markdown
# X Twitter Trends Scraper

This project is a Python-based web scraping application that fetches trending topics from Twitter (X.com) using **Selenium** and stores them in a MongoDB database. The application is powered by a **Flask** backend, making it easy to run locally and provide API endpoints for retrieving trends.

## Project Structure

Here’s an overview of the project structure:

```
X-twitter-trends-scrapping/
│
├── app.py                # Main Flask application
├── selenium_script.py    # Main script for Selenium-based scraping
├── config.py             # File for storing sensitive details securely
├── requirements.txt      # Python dependencies
├── templates/
│   └── index.html        # Frontend HTML file for displaying trends
├── .env                  # Environment variables (optional)
├── README.md             # Documentation (you are reading this)
└── ...
```

## Features

1. **Selenium-Based Scraping**: Fetches live trending topics from Twitter using the Selenium WebDriver.
2. **Scraper API**: Uses **ScraperAPI** as a proxy service to bypass restrictions like captchas, avoiding the need for paid mesh proxy services.
3. **MongoDB Integration**: Stores the fetched trends in a MongoDB database.
4. **Flask Backend**: Provides an easy-to-use API and local hosting for managing trends.
5. **Frontend UI**: Displays the fetched trends on a simple web interface (`index.html`).

## Why ScraperAPI?  
While **mesh proxy services** were initially considered, they required payments, and for this project, **ScraperAPI** provided a cost-effective solution for bypassing captchas and restrictions.

## Setup Instructions

Follow these steps to set up the project locally:

### 1. Clone the Repository
```bash
git clone https://github.com/nitininhouse/X-twitter-trends-scrapping.git
cd X-twitter-trends-scrapping
```

### 2. Install Dependencies
Ensure Python is installed (version 3.9+ is recommended). Install the required packages using:
```bash
pip install -r requirements.txt
```

### 3. Configure the Environment
#### Option 1: Using `config.py`
Edit the `config.py` file and add your sensitive details like:
```python
API_KEY = "your_scraperapi_key"
USERNAME = "your_twitter_username"
PASSWORD = "your_twitter_password"
MONGO_URI = "your_mongo_db_uri"
CHROMEDRIVER_PATH = "path_to_your_chromedriver"
```

#### Option 2: Using `.env` (Optional)
Alternatively, you can store sensitive details in a `.env` file:
```env
API_KEY=your_scraperapi_key
USERNAME=your_twitter_username
PASSWORD=your_twitter_password
MONGO_URI=your_mongo_db_uri
CHROMEDRIVER_PATH=path_to_your_chromedriver
```

Ensure you use the `dotenv` module to load these variables if you use `.env`.

### 4. Run the Selenium Script
The main scraping logic is in `selenium_script.py`. Run the script to scrape trending topics:
```bash
python selenium_script.py
```

### 5. Run the Flask App
Start the Flask app to host the backend API and frontend interface:
```bash
python app.py
```

The app will run locally at `http://127.0.0.1:5000/`.

### 6. Access the Frontend
Open your browser and visit `http://127.0.0.1:5000/` to view the trends on the frontend (`index.html`).

## Endpoints

- **`/fetch-trends`**: Fetches trending topics using Selenium and stores them in MongoDB.
- **`/`**: Displays the frontend interface.

## Tech Stack

- **Backend**: Flask
- **Scraping**: Selenium with ScraperAPI
- **Database**: MongoDB
- **Frontend**: HTML (in `templates/index.html`)

## Limitations

- **Proxy Costs**: While ScraperAPI is free to some extent, advanced usage may require an upgrade.
- **Twitter Restrictions**: Changes in Twitter (X.com) may require adjustments to the scraping logic.

## Repository
You can find the repository [here on GitHub](https://github.com/nitininhouse/X-twitter-trends-scrapping).

## Contribution
Feel free to fork the repository, make your changes, and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## License
This project is open-source and available under the [MIT License](LICENSE).
```
