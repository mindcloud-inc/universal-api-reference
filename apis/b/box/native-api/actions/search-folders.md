# Search Folders with Box

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.box.com/2.0`
- **Official documentation:** [Search Folders](https://developer.box.com/reference/get-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The text to search for in folder names and folder metadata. |
| `ancestor_folder_ids` | query | `string` | no | Optional comma-separated parent folder IDs to limit the search scope. |
| `limit` | query | `number` | no | Maximum number of folder search results to return. |
| `offset` | query | `number` | no | Offset-based pagination start position for folder search results. |
| `fields` | query | `string` | no | Optional comma-separated list of folder fields to include. |
| `sort` | query | `string` | no | Optional search sort field: relevance or modified_at. |
| `direction` | query | `string` | no | Search sort direction: DESC or ASC. |
