# List Market Holidays with Finnhub

Retrieves market holidays from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/market-holiday`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Market Holidays](https://finnhub.io/docs/api#market-holiday)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Exchange code for market holidays, such as US. |
