# Update Knowledge Note with Devin

Updates an existing knowledge note in Devin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/organizations/:org_id/knowledge/notes/:note_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Update Knowledge Note](https://docs.devin.ai/api-reference/v3/notes/put-organizations-knowledge-notes-note-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Knowledge note body. |
| `name` | body | `string` | yes | Knowledge note name. |
| `note_id` | path | `string` | yes | Knowledge note ID. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `trigger` | body | `string` | yes | Knowledge note trigger text. |
