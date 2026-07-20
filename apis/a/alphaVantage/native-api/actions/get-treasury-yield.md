# Get Treasury Yield with Alpha Vantage

Retrieves treasury yield data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Treasury Yield](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for TREASURY_YIELD. Accepted values: `0`, `1`, `2`. |
| `maturity` | query | `string` | yes | Query parameter $key for TREASURY_YIELD. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
