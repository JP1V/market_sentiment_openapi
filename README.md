# Market Sentiment API
[![RapidAPI](https://img.shields.io/badge/RapidAPI-Get%20Started-blue)](https://rapidapi.com/JP1V/api/market-sentiment1)
[![OpenAPI](https://img.shields.io/badge/OpenAPI-3.1-green)](https://jp1v.github.io/market_sentiment_openapi/)

AI-powered financial news sentiment for stocks, commodities, ETFs, and macro assets. Pass a ticker, get a bullish/bearish/neutral signal with confidence score and plain-English summary, sourced from Reuters, Bloomberg, CNBC, Financial Times, BBC News, and Al Jazeera, updated every 5 minutes.

### 1. Get your API key
[Subscribe on RapidAPI](https://rapidapi.com/JP1V/api/market-sentiment1) (Free tier available)

### 2. Make your first request
```bash
curl --request GET \
  --url 'https://market-sentiment-api.p.rapidapi.com/news/AAPL' \
  --header 'X-RapidAPI-Key: YOUR_API_KEY' \
  --header 'X-RapidAPI-Host: market-sentiment-api.p.rapidapi.com'
```

## Example Response

```json
{
  "ticker": "AAPL",
  "overall_sentiment": "bullish",
  "overall_sentiment_score": 0.85,
  "overall_confidence": 0.91,
  "sentiment_momentum": "increasing",
  "articles_analysed": 3,
  "summary": "Strong AI chip demand and positive macro sentiment drove bullish signals for AAPL.",
  "signals": [...]
}
```

## Endpoints

| Endpoint | Description |
|----------|-------------|
| `GET /news/{ticker}` | AI sentiment analysis for a ticker |
| `GET /news` | All current articles with signals |
| `GET /health` | Health check |

## Supported Assets

| Type | Examples |
|------|---------|
| Stocks | AAPL, TSLA, BP, MU |
| Commodities | CL=F, GC=F, NG=F |
| Sector ETFs | SOXX, XLE, XLF, JETS |
| Macro | SPY, QQQ, TLT, DXY |
| Currencies | EURUSD |

## Pricing

| Tier | Requests/month | Price |
|------|---------------|-------|
| Free | 50 | $0 |
| Tier 1 | 0–1,000 | $0.04/req |
| Tier 2 | 1,001–2,500 | $0.035/req |
| Tier 3 | 2,501–10,000 | $0.03/req |
| Tier 4 | 10,000+ | $0.025/req |

## Notes

- Returns neutral sentiment with `overall_confidence: 0.0` when no recent news is found, no error handling needed
- Sentiment derived from headlines and descriptions, not full article text
- Not financial advice

---

[Full Documentation →](https://jp1v.github.io/market_sentiment_openapi/) · Contact: ozhaya@proton.me
