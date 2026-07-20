# List Designs By Category with Abyssale

Retrieves designs from Abyssale by category.

## Endpoint

- **Method:** `GET`
- **Path:** `/designs`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [List Designs By Category](https://developers.abyssale.com/rest-api/designs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category_id` | query | `string` | yes | Unique identifier (UUID) of a category. Filter designs by a category. |
