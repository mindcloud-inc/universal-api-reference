# Update Article with Helpjuice

Updates an existing article in Helpjuice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/articles/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Article](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional updated article description. |
| `id` | path | `number` | yes | The Helpjuice article ID to update. |
| `name` | body | `string` | no | Optional updated article title. |
| `accessibility` | body | `number` | no | Optional accessibility value: 1 public, 0 internal, 2 private. |
