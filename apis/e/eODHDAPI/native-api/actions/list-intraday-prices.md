# List Intraday Prices with EODHD

Retrieves intraday prices for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/intraday/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List Intraday Prices](https://eodhd.com/financial-apis/intraday-historical-data-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
| `interval` | query | `string` | no | Intraday interval, such as `1m`, `5m`, or `1h`. |
| `from` | query | `date` | no | Start date/time accepted by EODHD intraday history. |
| `to` | query | `date` | no | End date/time accepted by EODHD intraday history. |
