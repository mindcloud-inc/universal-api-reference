# Update Category with BlogIn

Updates an existing category in BlogIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories/:id`
- **Base URL:** `https://blogin.co/api/rest`
- **Official documentation:** [Update Category](https://blogin.co/api/rest/docs/#update-a-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the category to update. |
| `name` | body | `string` | yes | The name of the category. |
| `position` | body | `number` | no | The position of the category. |
| `locked` | body | `boolean` | no | Whether the category is locked. |
