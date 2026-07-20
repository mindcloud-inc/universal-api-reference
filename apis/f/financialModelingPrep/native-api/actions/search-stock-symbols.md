# Search Stock Symbols with Financial Modeling Prep

Finds stock symbols in Financial Modeling Prep by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search-symbol`
- **Base URL:** `https://financialmodelingprep.com/stable`
- **Official documentation:** [Search Stock Symbols](https://site.financialmodelingprep.com/developer/docs/stable/search-symbol)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Ticker symbol or company name to search for, such as AAPL. |
