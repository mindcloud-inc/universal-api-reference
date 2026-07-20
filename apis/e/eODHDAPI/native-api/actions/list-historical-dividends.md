# List Historical Dividends with EODHD

Retrieves historical dividends for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/div/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Historical Dividends](https://eodhd.com/financial-apis/api-splits-dividends/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
| `from` | query | `date` | no | Start date in `YYYY-MM-DD` format. |
| `to` | query | `date` | no | End date in `YYYY-MM-DD` format. |
