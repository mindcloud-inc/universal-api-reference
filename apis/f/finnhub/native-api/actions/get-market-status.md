# Get Market Status with Finnhub

Retrieves market status from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/market-status`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Get Market Status](https://finnhub.io/docs/api#market-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange code for current market status, such as US. |
