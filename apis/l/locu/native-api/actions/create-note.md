# Create Note with Locu

Creates a new note in Locu.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Create Note](https://locu.app/api/docs#tag/notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Optional custom ID for the note |
| `text` | body | `string` | yes | Initial markdown text content |
| `icon` | body | `string` | no | Icon for the note |
| `color` | body | `string` | no | Hex color for the icon |
| `folderId` | body | `string` | no | Parent folder ID |
| `keepBreaks` | body | `boolean` | no | Preserve extra blank lines as empty paragraphs |
