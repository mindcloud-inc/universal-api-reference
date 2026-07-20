# List Series Categories with Federal Reserve Economic Data

Retrieves categories for a series from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/series/categories`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Series Categories](https://fred.stlouisfed.org/docs/api/fred/series_categories.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `series_id` | query | `string` | yes | The id for a series. |
