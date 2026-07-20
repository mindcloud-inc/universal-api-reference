# Update Category with Helpjuice

Updates an existing category in Helpjuice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/categories/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Category](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessibility` | body | `number` | no | The Helpjuice category accessibility. |
| `codename` | body | `string` | no | The Helpjuice category codename. |
| `description` | body | `string` | no | The Helpjuice category description. |
| `id` | path | `number` | yes | The Helpjuice category id. |
| `name` | body | `string` | no | The Helpjuice category name. |
