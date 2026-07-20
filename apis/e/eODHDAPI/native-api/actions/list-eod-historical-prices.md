# List EOD Historical Prices with EODHD

Retrieves end-of-day historical prices for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/eod/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [List EOD Historical Prices](https://eodhd.com/financial-apis/api-for-historical-data-and-volumes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
| `from` | query | `date` | no | Start date in `YYYY-MM-DD` format. |
| `to` | query | `date` | no | End date in `YYYY-MM-DD` format. |
| `period` | query | `string` | no | Historical price period, such as `d`, `w`, or `m`. |
