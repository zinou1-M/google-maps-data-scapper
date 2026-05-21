# Google-Maps-Scrapper
This Python script utilizes the Playwright library to perform web scraping and data extraction from Google Maps. It is particularly designed for obtaining information about businesses, including their name, address, website, phone number, reviews, and more.

## Read Prerequistes
Latest python was not used and is not suggested

<br>
To do a custom web scraping project you can find me on instagram or on telegram<br><br>

<a href="https://www.instagram.com/zinou.miloudi/" target="_blank">

<a href="https://t.me/ZinouMLD" target="_blank">


## Table of Contents
- [Prerequisites](#prerequisites)
- [Multiple Branches](#multiple-branches)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [Notes](#notes)
- [Video Example](#video-example)

## Prerequisites
- Python 3.8 or 3.9 (Python 3.10+ may not be compatible with some dependencies)
- Google Chrome or Chromium browser installed (for Playwright)

## Multiple Branches
The repo currently has 3 branches
- Main
- Latest Libraries (The one that works with latest libraries, can cause issues. Prefer Main)
- Linux ( Linux Support if main branch does not work correctly)


## Key Features
- Data Scraping: The script scrapes data from Google Maps listings, extracting valuable information about businesses, such as their name, address, website, and contact details.

- Review Analysis: It extracts review counts and average ratings, providing insights into businesses' online reputation.

- Business Type Detection: The script identifies whether a business offers in-store shopping, in-store pickup, or delivery services.

- Operating Hours: It extracts information about the business's operating hours.

- Introduction Extraction: The script also scrapes introductory information about the businesses when available.

- Data Cleansing: It cleanses and organizes the scraped data, removing redundant or unnecessary columns.

- CSV Export: The cleaned data is exported to a CSV file for further analysis or integration with other tools.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/zinou1-M/google-maps-data-scrapper.git
   ```
2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Install Playwright browsers:
   ```bash
   pip install playwright
   ```

## Usage

Run the script with your desired search term and number of results:

```bash
python main.py -s "magasin de meuble" -t 20
```

- `-s` or `--search`: Search query for Google Maps (default: "magasin de meuble oran")
- `-t` or `--total`: Number of results to scrape (default: 20)
- `-o` or `--output`: Output CSV file path (default: result.csv)
- `--append`: Append results to the output file instead of overwriting (default: off)

## Example

Append new results to an existing CSV file:
```bash
python main.py -s "magasin de meuble oran" -t 20 -o result.csv --append
```

The script will launch a browser, perform the search, and start scraping information. Progress will be displayed in the terminal, and results will be saved to the specified CSV file. If `--append` is used, new results will be added to the end of the file without removing previous data.

## Notes
- The script opens a visible browser window (not headless) for scraping.
- Google Maps DOM may change, which can break the script. If you encounter issues, update the XPaths in `main.py`.
- Avoid running too many scrapes in a short period to prevent being blocked by Google.


## License
MIT
