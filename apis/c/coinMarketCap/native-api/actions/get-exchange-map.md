# Get Exchange Map with CoinMarketCap

Retrieves exchange IDs and slugs from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/exchange/map`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Exchange Map](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-exchange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | no | Exchange slug, for example binance. |
