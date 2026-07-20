# Create Category with Tettra

Creates a new category in Tettra.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/85329/categories`
- **Base URL:** `https://app.tettra.co/api`
- **Official documentation:** [Create Category](https://support.tettra.com/categories-and-subcategories/api-endpoint-create-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Category description. |
| `name` | body | `string` | yes | Category name. |
