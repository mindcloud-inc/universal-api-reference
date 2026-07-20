# Get News Sentiment with Alpha Vantage

Retrieves news sentiment data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get News Sentiment](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Query parameter $key for NEWS_SENTIMENT. |
| `tickers` | query | `string` | yes | Query parameter $key for NEWS_SENTIMENT. |
| `time_from` | query | `string` | no | Query parameter $key for NEWS_SENTIMENT. |
