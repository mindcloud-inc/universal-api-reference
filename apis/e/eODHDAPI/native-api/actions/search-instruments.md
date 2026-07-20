# Search Instruments with EODHD

Finds instruments in EODHD API by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/{query}`
- **Base URL:** `https://eodhd.com/api`
- **Official documentation:** [Search Instruments](https://eodhd.com/financial-apis/search-api-for-stocks-etfs-mutual-funds-and-indices/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | path | `string` | yes | Search query text for ticker, company, ETF, fund, or index lookup. |
