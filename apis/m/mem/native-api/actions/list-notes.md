# List Notes with Mem

Retrieves notes from Mem.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/notes`
- **Base URL:** `https://api.mem.ai`
- **Official documentation:** [List Notes](https://docs.mem.ai/api-reference/notes/list-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_by` | query | `string` | no | Optional note ordering. |
| `filters` | query | `object` | no | Optional note filters. |
| `filters.note_visibility` | query | `string` | no | — |
| `filters.collection_ids` | query | `list<string>` | no | — |
| `filters.contains_open_tasks` | query | `boolean` | no | — |
| `filters.contains_tasks` | query | `boolean` | no | — |
| `filters.contains_images` | query | `boolean` | no | — |
| `filters.contains_files` | query | `boolean` | no | — |
| `include_note_content` | query | `boolean` | no | — |
