# Search Stories with Shortcut

## Endpoint

- **Method:** `GET`
- **Path:** `/search/stories`
- **Base URL:** `https://api.app.shortcut.com/api/v3`
- **Official documentation:** [Search Stories](https://developer.shortcut.com/api/rest/v3#Search-Stories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The search query to run against stories. |
| `detail` | query | `string` | no | The level of detail to return for matched stories. |
| `entity_types` | query | `list<string>` | no | Limit the search to specific entity types. |
