# Get Index Data with Alpha Vantage

Retrieves index time series data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Index Data](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for INDEX_DATA. |
| `symbol` | query | `string` | yes | Query parameter $key for INDEX_DATA. |
