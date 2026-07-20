# Create Article with Helpjuice

Creates a new article in Helpjuice.

## Endpoint

- **Method:** `POST`
- **Path:** `/articles`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Article](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional article description. |
| `name` | body | `string` | yes | The article title. |
| `categoryId` | body | `number` | yes | The category ID to assign to the article. |
| `accessibility` | body | `number` | no | Optional accessibility value: 1 public, 0 internal, 2 private. |
