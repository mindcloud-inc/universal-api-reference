# Get Valuation Metrics with EODHD

Retrieves valuation metrics for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/fundamentals/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Valuation Metrics](https://eodhd.com/financial-apis/stock-etfs-fundamental-data-feeds/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
