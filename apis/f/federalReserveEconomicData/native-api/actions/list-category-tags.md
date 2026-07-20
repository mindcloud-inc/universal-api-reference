# List Category Tags with Federal Reserve Economic Data

Retrieves category tags from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/category/tags`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Category Tags](https://fred.stlouisfed.org/docs/api/fred/category_tags.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | query | `number` | yes | The id for a category. |
