# Get News Sentiment with Finnhub

Retrieves news sentiment from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/news-sentiment`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Get News Sentiment](https://finnhub.io/docs/api#news-sentiment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | yes | US company symbol for news sentiment, such as AAPL. |
