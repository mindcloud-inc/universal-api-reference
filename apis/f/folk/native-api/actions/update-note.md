# Update Note with folk

Updates an existing note in folk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/notes/:noteId`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Update Note](https://developer.folk.app/api-reference/notes/update-a-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `noteId` | path | `string` | yes | The ID of the note to update. |
| `content` | body | `string` | no | The updated content of the note. |
| `visibility` | body | `string` | no | The updated note visibility. Supported values are public or private. |
