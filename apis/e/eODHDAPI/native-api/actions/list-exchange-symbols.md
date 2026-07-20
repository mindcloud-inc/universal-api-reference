# List Exchange Symbols with EODHD

Retrieves symbols for an exchange from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/exchange-symbol-list/{exchangeCode}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Exchange Symbols](https://eodhd.com/financial-apis/exchanges-api-list-of-tickers-and-trading-hours/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchangeCode` | path | `string` | yes | EODHD exchange code, such as `US`, `LSE`, `CC`, or `FOREX`. |
