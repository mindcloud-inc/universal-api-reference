# Get Note with LunaNotes

Retrieves a note from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/notes/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Note](https://lunanotes.io/docs/notes/get-v1-notes-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes note ID. |
| `include` | query | `string` | no | Comma-separated: tags,video. |
