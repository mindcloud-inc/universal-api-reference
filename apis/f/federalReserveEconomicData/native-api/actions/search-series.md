# Search Series with Federal Reserve Economic Data

Finds series in Federal Reserve Economic Data by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/series/search`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [Search Series](https://fred.stlouisfed.org/docs/api/fred/series_search.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_text` | query | `string` | yes | The words to match against economic data series. |
| `search_type` | query | `string` | no | Determines the type of search to perform. |
