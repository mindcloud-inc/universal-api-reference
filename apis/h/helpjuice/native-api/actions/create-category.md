# Create Category with Helpjuice

Creates a new category in Helpjuice.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Category](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codename` | body | `string` | no | Optional category codename/slug. |
| `description` | body | `string` | no | Optional category description. |
| `name` | body | `string` | yes | The category name. |
| `accessibility` | body | `number` | no | Optional accessibility value: 1 public, 0 internal, 2 private. |
