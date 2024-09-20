# StockRecommenderSystem

## Live Demo
Check out the live demo of the app here: [Live Demo](https://stockrecommendation-mcve.onrender.com)

## Overview
In this project, I aimed to apply the Discounted Cash Flow (DCF) model to stock evaluation, providing users with a systematic way to determine whether a stock is undervalued, overvalued, or fairly valued. DCF is a well-established financial valuation method (also pondered upon by giant investor Warren Buffet) that calculates the present value of expected future cash flows to determine the intrinsic value of a stock. By comparing this intrinsic value to the current market price, investors can make informed decisions about buying, holding, or selling. The fundamental logic is if the intrinic value of stock is greater than its market capitalization, is suggests a Buy, if it is less than market cap it suggests a Sell and else a Hold.

The system integrates Mistral.AI Large 2 to generate a short summary for each stock based on its intrinsic value, enhancing the user experience with personalized insights. The project also features a frontend interface that allows users to visualize financial data and perform stock analysis in real-time.

## Features
Stock Analysis: Calculates intrinsic value based on DCF model using real-time financial statements.
Buy/Sell Recommendation: Provides recommendations based on the intrinsic value and market cap.
AI Integration: Automatically generates a summary about the stock based on its financials.
Financial Data Visualization: Charts that visualize historical stock prices, cash flows, balance sheets and income statements.
Interactive Web Application: Intuitive user interface built with Flask for backend, and jQuery/Chart.js for frontend.
API Integration: Fetches financial data using Financial Modeling Prep API.

Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/stock-recommender-system.git
cd stock-recommender-system
Create a virtual environment and install dependencies:

bash
Copy code
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
Set up environment variables for the API keys:

bash
Copy code
export OPENAI_API_KEY="your_openai_api_key"
export FMP_API_KEY="your_fmp_api_key"
Run the Flask server:

bash
Copy code
flask run
Open the app in your browser at http://127.0.0.1:5000.

Usage
Stock Analysis:

Enter a stock ticker symbol (e.g., AAPL) to fetch and display financial statements.
View DCF-based recommendations on whether to buy, sell, or hold the stock.
GPT-3.5 Summaries:

After DCF analysis, the app generates a brief summary of the stock based on its intrinsic value.
Visualizations:

View stock price trends, balance sheets, income statements, and cash flow statements.
File Structure
php
Copy code
.
├── app.py                     # Backend logic and routes
├── templates/
│   └── index.html             # Frontend page
├── static/
│   ├── css/                   # CSS files
│   └── js/                    # JavaScript for dynamic updates and API calls
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation
API Endpoints
/api/scrape: Fetches financial data (balance sheet, income statement, cash flow).
/api/calculate_dcf: Calculates the intrinsic value and provides stock recommendations.
/api/generate_summary: Uses GPT-3.5 to generate a stock summary.
Future Improvements
Machine Learning: Integrate ML algorithms to improve stock recommendation accuracy.
Portfolio Management: Enable users to create and manage stock portfolios.
Real-time Alerts: Notify users when a stock's price crosses its intrinsic value threshold.
## Technologies Used
Frontend: HTML, CSS, JavaScript, AJAX, Chart.js
Backend: Python (Flask)
Web Scraping: BeautifulSoup, Requests
Data Visualization: Chart.js
Containerization: Docker
Version Control: Git, Github
Hosting/Deployment: Render
Web Scraping APIs : [Financial Modelling Prep](https://site.financialmodelingprep.com/developer/docs),
                    [Yahoo Finance](https://finance.yahoo.com/)
LLM model : Mistral.AI - mistral-large-latest
