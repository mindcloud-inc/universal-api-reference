# Search Workspace with Awork

Finds workspace entities in Awork by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Search Workspace](https://developers.awork.com/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchTerm` | query | `string` | yes | Search text to match across the selected resource types. |
| `searchTypes` | query | `string` | no | Comma-separated resource types to search in awork. |
| `top` | query | `number` | no | Maximum number of search results to return. |
| `includeClosedAndStuck` | query | `boolean` | no | Whether to include closed and stuck entities in search results. |
