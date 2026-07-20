# Get OBV Indicator with Alpha Vantage

Retrieves OBV indicator data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get OBV Indicator](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `interval` | query | `string` | yes | Query parameter $key for OBV. |
| `symbol` | query | `string` | yes | Query parameter $key for OBV. |
