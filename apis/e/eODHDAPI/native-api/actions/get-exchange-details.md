# Get Exchange Details with EODHD

Retrieves trading hours and holidays for an exchange from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/exchange-details/{exchangeCode}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Exchange Details](https://eodhd.com/financial-apis/exchanges-api-trading-hours-and-stock-market-holidays/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchangeCode` | path | `string` | yes | EODHD exchange code for exchange details. |
