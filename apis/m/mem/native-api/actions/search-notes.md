# Search Notes with Mem

Finds notes in Mem by search query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/notes/search`
- **Base URL:** `https://api.mem.ai`
- **Official documentation:** [Search Notes](https://docs.mem.ai/api-reference/notes/search-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Search query text. |
| `filters` | body | `object` | no | Optional search filters. |
| `filters.by_collection_ids` | body | `list<string>` | no | — |
| `filters.contains_open_tasks` | body | `boolean` | no | — |
| `filters.contains_tasks` | body | `boolean` | no | — |
| `filters.contains_images` | body | `boolean` | no | — |
| `filters.contains_files` | body | `boolean` | no | — |
