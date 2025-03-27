# SEC 8-K Product Announcement Extractor

This project was developed as part of an academic assignment focused on using Large Language Models (LLMs) and natural language processing to extract product release information from SEC Form 8-K filings.

## 🔗 GitHub Repository
https://github.com/chackbarth/sec-8k-extraction

## 📌 Objective
The goal was to programmatically identify and extract new product announcements from the most recent 8-K filings of S&P 500 companies. The output includes:
- Company name
- Ticker
- Filing date
- New product (if mentioned)
- Short description of the product

## 🧠 Technologies Used
- Python 3
- OpenAI GPT-3.5 API
- BeautifulSoup for HTML parsing
- SEC EDGAR Atom feeds
- CSV for structured output

## 🛠️ How It Works

1. Load 500 companies from the SEC's `company_tickers.json`.
2. For each company:
   - Retrieve its latest 8-K filing using the SEC Atom feed.
   - Locate the `.txt` submission file from the filing index page.
   - Send a prompt to the OpenAI API to summarize any new product mentions.
3. Write results into a CSV file.

## 📁 Files Included
- `sec_8k_extractor.ipynb` – Main Jupyter Notebook (can also be run as a Python script)
- `sec_8k_product_extractions.csv` – Output file with extracted data
- `Hackbarth_Chandler_SEC_Methodology.docx` – Written methodology report
- `README.md` – This file

## ▶️ Running the Script

Install dependencies:

```bash
pip install -r requirements.txt
```

Or manually install:

```bash
pip install openai beautifulsoup4 requests
```

Then run the notebook or Python script.

## 📤 Output Example

| company_name | stock_name | filing_time | new_product     | product_description                 |
|--------------|------------|--------------|------------------|--------------------------------------|
| Apple Inc.   | AAPL       | 2025-02-25   | Apple Vision Pro | Spatial computing headset unveiled   |

## 📬 Contact

Created by **Chandler Hackbarth**  
Email: chandlerhackbarth@gmail.com  
GitHub: [https://github.com/chackbarth](https://github.com/chackbarth)
