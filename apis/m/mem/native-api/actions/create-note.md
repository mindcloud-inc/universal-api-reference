# Create Note with Mem

Creates a new note in Mem.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/notes`
- **Base URL:** `https://api.mem.ai`
- **Official documentation:** [Create Note](https://docs.mem.ai/api-reference/notes/create-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The note content to save. |
| `id` | body | `string` | no | Optional note ID. |
| `collection_ids` | body | `list<string>` | no | Optional collection IDs to attach to the note. |
| `collection_titles` | body | `list<string>` | no | Optional collection titles to attach to the note. |
| `created_at` | body | `date` | no | — |
| `updated_at` | body | `date` | no | — |
