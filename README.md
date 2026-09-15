# Wikiquote Scraper

A small NLP project for scraping Wikiquote pages and experimenting with neural text generation.

## Overview

The project contains two related workflows:

* **Multi-page scraping:** collects quotes from multiple Wikiquote pages and stores the extracted data in a JSON file.
* **Text generation:** scrapes a Wikiquote page, processes the extracted text, trains a neural language model, and generates text from a given seed.

The project was developed as an experiment with web scraping, text preprocessing, tokenization, and language modelling.

## Project Structure

```text
wikiquote-scraper/
├── notebooks/
│   ├── scrape_and_model.ipynb
│   └── wikiquote_scraper_multipage.ipynb
├── README.md
└── requirements.txt
```

### `wikiquote_scraper_multipage.ipynb`

Scrapes Wikiquote's list of pages and extracts quotes from multiple pages.

For each page, the scraper collects:

* page URL
* page title
* extracted quotes

The extracted text is cleaned to remove unwanted sections, labels, and formatting artifacts before being stored in the resulting JSON file.

### `scrape_and_model.ipynb`

Scrapes the quotes from a Wikiquote page and uses the resulting text to train a simple neural language model.

The workflow includes:

1. Scraping and extracting the page text.
2. Cleaning the extracted text.
3. Tokenizing the text.
4. Creating sequences for language-model training.
5. Training the model.
6. Generating text from a user-provided seed.

## Usage

The project is implemented in Jupyter notebooks.

Open the relevant notebook from the `notebooks/` directory and run the workflow. Wikiquote URLs and text-generation parameters can be adjusted directly in the notebooks.

## Data Source

The data is collected from [Wikiquote](https://it.wikiquote.org/).

The scraper is intended for educational and experimental use. Requests should be made at a reasonable rate and the applicable Wikimedia/Wikiquote policies should be respected.

Content retrieved from Wikiquote remains subject to the applicable licensing and attribution requirements.
