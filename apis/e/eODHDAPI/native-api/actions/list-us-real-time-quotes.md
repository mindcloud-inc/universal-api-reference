# List US Real-Time Quotes with EODHD

Retrieves real-time quotes for US symbols from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/real-time/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List US Real-Time Quotes](https://eodhd.com/financial-apis/bulk-for-live-ohlcv-stock-prices-api-us-exchanges-only/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | Representative ticker used with the `ex=US` bulk live quote request. |
