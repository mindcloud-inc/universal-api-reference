# Get Knowledge Note with Devin

Retrieves a knowledge note from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/knowledge/notes/:note_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Get Knowledge Note](https://docs.devin.ai/api-reference/v3/notes/get-organizations-knowledge-notes-note-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note_id` | path | `string` | yes | Knowledge note ID. |
| `org_id` | path | `string` | yes | Devin organization ID. |
