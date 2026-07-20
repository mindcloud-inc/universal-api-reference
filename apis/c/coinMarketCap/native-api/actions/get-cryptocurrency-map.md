# Get Cryptocurrency Map with CoinMarketCap

Retrieves cryptocurrency IDs and symbols from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cryptocurrency/map`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Cryptocurrency Map](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | query | `string` | no | Cryptocurrency slug filter, for example bitcoin. |
| `symbol` | query | `string` | no | Cryptocurrency symbol filter, for example BTC. |
