# Tradingview-chrome-extension

This chrome extension lets you automatically fetch and access interactive stock charts from TradingView
 using:

FastAPI for API endpoints

Selenium (with WebDriver Manager) for browser automation

LangChain (LLM) for parsing natural language into actions

It supports ticker lookup (e.g., MSFT, AAPL, TSLA) and timeframe switching (1D, 1M, 1Y, etc.).

✨ Features

✅ Gives you all the real time data for any particular stock
✅ Can give you related news headlines posted about any stock 
✅ Search for any stock ticker on TradingView
✅ Auto-open the growth chart of any particular stock asked
✅ Switch chart timeframe (1D, 5D, 1M, 3M, 6M, YTD, 1Y, 5Y, ALL)
✅ Works in headless or visible Chrome mode
✅ Can give you stocks of any sector you ask like Technology, manufacturing, finance etc.
✅ Logs all actions for debugging

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
