# Update Category with Swell

## Endpoint

- **Method:** `PUT`
- **Path:** `/categories/:id`
- **Base URL:** `https://api.swell.store`
- **Official documentation:** [Update Category](https://developers.swell.is/backend-api/categories/update-a-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Swell category ID. |
| `name` | body | `string` | no | The category name. |
| `active` | body | `boolean` | no | Whether the category is active. |
