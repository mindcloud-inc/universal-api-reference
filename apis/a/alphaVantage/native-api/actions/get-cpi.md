# Get CPI with Alpha Vantage

Retrieves CPI data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get CPI](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for CPI. Accepted values: `0`, `1`. |
