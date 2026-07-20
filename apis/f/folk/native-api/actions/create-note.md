# Create Note with folk

Creates a new note in folk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/notes`
- **Base URL:** `https://api.folk.app`
- **Official documentation:** [Create Note](https://developer.folk.app/api-reference/notes/create-a-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity.id` | body | `string` | yes | The ID of the entity the note belongs to. |
| `content` | body | `string` | yes | The content of the note. |
| `visibility` | body | `string` | yes | The note visibility. Supported values are public or private. |
