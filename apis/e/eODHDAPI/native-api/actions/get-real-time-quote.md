# Get Real-Time Quote with EODHD

Retrieves a real-time quote for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/real-time/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Real-Time Quote](https://eodhd.com/financial-apis/live-ohlcv-stocks-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
