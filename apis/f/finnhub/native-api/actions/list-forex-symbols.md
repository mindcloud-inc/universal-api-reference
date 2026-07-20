# List Forex Symbols with Finnhub

Retrieves forex symbols from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/forex/symbol`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Forex Symbols](https://finnhub.io/docs/api#forex-symbols)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `exchange` | query | `string` | yes | Forex exchange code, such as oanda. |
