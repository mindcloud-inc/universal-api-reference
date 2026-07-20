# Search Entities with FTrack

Searches entities in FTrack by terms and entity type.

## Endpoint

- **Method:** `POST`
- **Path:** `/api`
- **Base URL:** `{serverUrl}`
- **Official documentation:** [Search Entities](https://developer.ftrack.com/api/operations/search-api-search-search-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expression` | body | `string` | yes | Search expression to scope the results. |
| `terms[]` | body | `array<string>` | yes | Search terms as a list of strings. |
| `entity_type` | body | `string` | yes | Entity type to search, such as Task or AssetVersion. |
