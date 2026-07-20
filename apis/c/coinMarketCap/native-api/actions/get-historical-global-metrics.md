# Get Historical Global Metrics with CoinMarketCap

Retrieves historical global crypto market metrics from CoinMarketCap.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/global-metrics/quotes/historical`
- **Base URL:** `https://pro-api.coinmarketcap.com`
- **Official documentation:** [Get Historical Global Metrics](https://pro.coinmarketcap.com/api/documentation/ai-agent-hub/skills/cmc-api-market)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | no | Historical interval such as daily. |
| `time_end` | query | `string` | no | End date or timestamp for the historical window. |
| `time_start` | query | `string` | no | Start date or timestamp for the historical window. |
