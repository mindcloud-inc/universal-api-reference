# Get Historical Market Cap with EODHD

Retrieves historical market capitalization for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/historical-market-cap/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Historical Market Cap](https://eodhd.com/financial-apis/historical-market-capitalization-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
| `from` | query | `date` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `date` | no | End date in YYYY-MM-DD format. |
