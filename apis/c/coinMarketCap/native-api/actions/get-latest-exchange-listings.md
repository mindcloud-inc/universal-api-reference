# Get Latest Exchange Listings with CoinMarketCap

Retrieves latest exchange listings from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/exchange/listings/latest`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Latest Exchange Listings](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-exchange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of exchange listings to return. |
