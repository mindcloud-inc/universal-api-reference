# Create or Update Category with Loyverse

Creates or updates a category in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Create or Update Category](https://developer.loyverse.com/docs/#tag/Categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | The category id. If included in the POST request it will cause an update instead of a creating a new object. |
| `name` | body | `string` | yes | — |
| `color` | body | `string` | no | — |
| `created_at` | body | `date` | no | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `deleted_at` | body | `date` | no | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
