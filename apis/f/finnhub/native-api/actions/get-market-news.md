# Get Market News with Finnhub

Retrieves market news from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/news`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Get Market News](https://finnhub.io/docs/api#market-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | yes | Market news category: general, forex, crypto, or merger. |
| `minId` | query | `number` | no | Optional news ID lower bound for fetching newer items. |
