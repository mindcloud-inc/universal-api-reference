# Create Note with Reflect

Creates a new note in Reflect.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphs/:graphId/notes`
- **Base URL:** `https://reflect.app/api`
- **Official documentation:** [Create Note](https://openpm.ai/packages/reflect#/graphs/{graphId}/notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `graphId` | path | `list<string>` | yes | Your graph identifier |
| `subject` | body | `string` | yes | The subject of the note |
| `content_markdown` | body | `string` | yes | The content of the note in markdown |
| `pinned` | body | `boolean` | no | Whether the note should be pinned |
