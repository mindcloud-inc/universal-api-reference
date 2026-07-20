# Get Latest EOD Close with EODHD

Retrieves the latest end-of-day close for a symbol from EODHD API.

## Endpoint

- **Method:** `GET`
- **Path:** `/eod/{symbol}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Get Latest EOD Close](https://eodhd.com/financial-apis/api-for-historical-data-and-volumes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | path | `string` | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. |
