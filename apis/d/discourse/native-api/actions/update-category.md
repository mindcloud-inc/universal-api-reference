# Update Category with Discourse

Updates an existing category in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/categories/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Category](https://docs.discourse.org/#tag/Categories/operation/updateCategory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Category id. |
| `name` | body | `string` | yes | Category name. |
| `color` | body | `string` | no | Category color hex code without #. |
