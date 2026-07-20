# Delete Knowledge Note with Devin

Deletes an existing knowledge note from Devin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/organizations/:org_id/knowledge/notes/:note_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Delete Knowledge Note](https://docs.devin.ai/api-reference/v3/notes/delete-organizations-knowledge-notes-note-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note_id` | path | `string` | yes | Knowledge note ID. |
| `org_id` | path | `string` | yes | Devin organization ID. |
