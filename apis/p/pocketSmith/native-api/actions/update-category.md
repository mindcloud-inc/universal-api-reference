# Update Category with PocketSmith

Updates a PocketSmith category.

## Endpoint

- **Method:** `PUT`
- **Path:** `/categories/:id`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [Update Category](https://developers.pocketsmith.com/reference/put_categories-id-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `colour` | body | `string` | no | A new CSS-style hex colour for the category. |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith category. |
| `title` | body | `string` | no | A new title for the category. |
