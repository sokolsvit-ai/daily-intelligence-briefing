# 🤖 AI Daily Intelligence Briefing (n8n Automation)

An advanced automated multi-source data aggregator built in **n8n**. It collects real-time data on weather, currency exchange rates, cryptocurrency, stock markets, and news, then processes everything via **Google Gemini LLM** to generate and deliver a comprehensive daily morning briefing straight to **Telegram**.

## 🏗 Workflow Architecture
1. **Schedule Trigger:** Automatically kicks off the workflow every morning at 07:00.
2. **Parallel API Data Fetching:** Multiple HTTP Request nodes simultaneously fetch data from external APIs for:
   - Weather & Air Quality (Lutsk, Kyiv, Valencia)
   - Currency Rates (USD/EUR, NBU) & Crypto Prices (BTC, ETH) + Fear & Greed Index
   - Stock Market Indices (S&P 500, NASDAQ, Dow Jones)
   - News Feeds, Quotes, Holidays, and Historical Events
3. **Data Normalization & Aggregation:** Custom JavaScript and Merge nodes clean and combine all incoming JSON payloads.
4. **AI Processing (Google Gemini LLM):** Summarizes the collected data into an engaging daily digest.
5. **Telegram Delivery:** Sends the final formatted briefing directly to a Telegram channel or chat.

## 🛠 Tech Stack
- **Automation Core:** n8n
- **AI Integration:** Google Gemini API (LLM Chain)
- **Data Sources:** Multiple REST APIs (Weather, Finance, News, Crypto)
- **Output Channel:** Telegram Bot API

## 🚀 How to Set Up
1. Import the `workflow.json` file into your n8n instance.
2. Set up your **Google Gemini API** credentials.
3. Configure your **Telegram Bot** token and destination chat ID.
4. Adjust or plug in API keys for weather and financial data providers if needed.

📩 **Contact & Custom Solutions:** [My Telegram Channel](https://t.me/vladiksonchik)
