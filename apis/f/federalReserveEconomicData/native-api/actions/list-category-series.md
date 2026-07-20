# List Category Series with Federal Reserve Economic Data

Retrieves series for a category from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/category/series`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Category Series](https://fred.stlouisfed.org/docs/api/fred/category_series.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | query | `number` | yes | The id for a category. |
