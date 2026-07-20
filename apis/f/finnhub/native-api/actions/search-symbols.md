# Search Symbols with Finnhub

Finds symbols in Finnhub by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Search Symbols](https://finnhub.io/docs/api#symbol-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search text. Finnhub accepts a symbol, security name, ISIN, or CUSIP. |
| `exchange` | query | `string` | no | Optional exchange limit for symbol search. |
