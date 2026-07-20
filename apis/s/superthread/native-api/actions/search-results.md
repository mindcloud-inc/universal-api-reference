# Search Results with Superthread

## Endpoint

- **Method:** `GET`
- **Path:** `/:team_id/search`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Search Results](https://superthread.com/docs/api-docs/search/get-search-results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Include archived records in the search. |
| `fields` | query | `string` | no | Choose which fields Superthread should search. |
| `grouped` | query | `boolean` | no | Return grouped search results when enabled. |
| `project_id` | query | `string` | no | Limit results to one Superthread space or project. |
| `query` | query | `string` | yes | Search text to match across workspace content. |
| `statuses` | query | `string` | no | Limit card and epic search results to specific statuses. |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace to search. |
| `types` | query | `string` | no | Limit results to specific resource types. |
