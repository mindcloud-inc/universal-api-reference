# Create Note with Assembly.com

Creates a note in Assembly.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Create Note](https://docs.assembly.com/reference/create-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | body | `string` | yes | The type of entity that this note is associated with. |
| `entityId` | body | `string` | yes | The ID of the entity that this note is associated with. |
| `title` | body | `string` | yes | The note title. |
| `content` | body | `string` | no | The note content as valid HTML. |
