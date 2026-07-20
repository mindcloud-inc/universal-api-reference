# Get Technical Indicator with EODHD

Retrieves a technical indicator for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/technical/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Technical Indicator](https://eodhd.com/financial-apis/technical-indicators-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
| `function` | query | `string` | yes | Technical indicator function, for example sma. |
| `period` | query | `number` | no | Indicator calculation period. |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |
| `order` | query | `string` | no | Result order, for example d for descending. |
| `splitadjusted_only` | query | `boolean` | no | Return split-adjusted values only when supported. |
| `filter` | query | `string` | no | Optional response filter. |
