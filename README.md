# Tradingview-chrome-extension

This chrome extensionan is an AI-powered stock assistant that uses:

FastAPI – API server & endpoints

Selenium (with WebDriver Manager) – automate TradingView scraping

LangChain + Google Gemini – parse natural language queries into actions

Custom scraping utilities – fetch tickers, performance, news, sectors, and charts

It supports:

Querying best/worst performing stocks

Getting single stock details

Fetching latest stock news

Retrieving sector-wise data

Displaying interactive TradingView charts with chosen timeframes

✨ Features

✅ Gives you all the real time data for any particular stock

✅ Scrape stock lists from sector pages

✅ Extract single stock details (price, performance, stats)

✅ Scrape stock-related news hedlines

✅ Display interactive stock charts & switch timeframes automatically

✅ Click specific elements dynamically


🗂 Project Structure
.
├── app.py        # FastAPI server, routes requests
├── sel.py        # Selenium automation and scraping(chart display logic)
├── manifest.json 
├── popup.css
├── popup.html
├── popup.js
├── requirements.txt
└── README.md  

app.py
Runs the FastAPI server, Routes the users question, calls the Selenium automation accordingly, and responds.

sel.py
Contains all the functions for different categories of question which launches Chrome, 
searches the ticker on TradingView, gets insights, news, prices, market cap, best performing, worst performing stocks, charts etc.

⚙️ Installation

1. Clone the repo
  
2. Create & activate a virtual environment

3. Install dependencies



▶️ Usage

1. Firstly, Set up environment variables

Create a .env file in the project root:
GOOGLE_GEMINI_KEY=your_api_key_here

2. Unload the folder in chrome extension manager.

3. Run the FastAPI app
uvicorn app:app --reload

4. Open the extension named Stock chatbot in the chrome browser.

5. Enter your query and it will fetch the real time data


### Example Queries ###
🔹 Multiple Stocks (navigate + extract)

"Show me the best performing stocks today"

"Top 5 losing stocks in the US market"

"Which are the top 3 gainers in the stock market right now?"

"Show me 10 most active stocks"

🔹 Single Stock Details (navigate_single + extract_single)

"Show me Apple stock"

"Get Tesla stock details"

"What is the current price of Microsoft?"

"Infosys stock performance"

🔹 Stock News (actions_news → fetch_stock_news)

"Latest news on Apple"

"Show me 3 news articles about Tesla"

"Google stock news"

"NVIDIA news from the last week"

🔹 Stock Chart Display (actions_chart → display_chart)

"Show me Apple stock chart for 1 year"

"Tesla 6 months chart"

"MSFT 1M chart"

"NVIDIA stock chart YTD"

🔹 Sector Data (action_sector → fetch_sector_data)

"Show me all technology stocks"

"Top 5 energy sector stocks"

"Finance sector stock data"

"Which companies are in retail trade sector?"

🔹 General / Chit-Chat (Handled gracefully by LLM refine)

"Hi, how are you?"

"Who created you?"

"Can you tell me a joke?"

"Good morning!"

👉 Each of these queries maps internally to actions that trigger Selenium scraping + LangChain refinement.


📜 License

MIT License - free to use.
