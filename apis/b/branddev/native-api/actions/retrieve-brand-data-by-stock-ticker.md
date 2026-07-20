# Retrieve Brand Data by Stock Ticker with Brand.dev

Retrieves brand data from Brand.dev by stock ticker.

## Endpoint

- **Method:** `GET`
- **Path:** `/brand/retrieve-by-ticker`
- **Base URL:** `https://api.brand.dev/v1`
- **Official documentation:** [Retrieve Brand Data by Stock Ticker](https://docs.context.dev/api-reference/retrieve-brand/retrieve-brand-data-by-stock-ticker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticker` | query | `string` | yes | Stock ticker symbol to retrieve brand data for. |
