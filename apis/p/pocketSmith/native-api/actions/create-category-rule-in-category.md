# Create Category Rule In Category with PocketSmith

Creates a category rule for a PocketSmith category.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories/:id/category_rules`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [Create Category Rule In Category](https://developers.pocketsmith.com/reference/post_categories-id-category-rules-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith category. |
| `payee_matches` | body | `string` | yes | The keyword or keywords to match the transaction payees. |
