# Get Historical Options with Alpha Vantage

Retrieves historical options data from Alpha Vantage.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Get Historical Options](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Query parameter $key for HISTORICAL_OPTIONS. |
| `symbol` | query | `string` | yes | Query parameter $key for HISTORICAL_OPTIONS. |
