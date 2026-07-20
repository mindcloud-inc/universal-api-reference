# Get Cryptocurrency Gainers and Losers with CoinMarketCap

Retrieves cryptocurrency gainers and losers from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cryptocurrency/trending/gainers-losers`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Cryptocurrency Gainers and Losers](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-crypto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of gainers and losers records to return. |
