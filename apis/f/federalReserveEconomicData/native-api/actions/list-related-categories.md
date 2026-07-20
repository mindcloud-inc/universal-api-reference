# List Related Categories with Federal Reserve Economic Data

Retrieves related categories from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/category/related`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Related Categories](https://fred.stlouisfed.org/docs/api/fred/category_related.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | query | `number` | yes | The id for a category. |
