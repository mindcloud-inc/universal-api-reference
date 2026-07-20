# Search Symbols with Alpha Vantage

Finds symbols in Alpha Vantage by keywords.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `https://www.alphavantage.co`
- **Official documentation:** [Search Symbols](https://www.alphavantage.co/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords` | query | `string` | yes | Query parameter $key for SYMBOL_SEARCH. |
| `datatype` | query | `string` | no | Optional response format. Leave unset for JSON. Accepted values: `0`, `1`. |
