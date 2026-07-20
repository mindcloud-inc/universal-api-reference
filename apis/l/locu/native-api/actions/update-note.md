# Update Note with Locu

Updates an existing note in Locu.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/notes/:id`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Update Note](https://locu.app/api/docs#tag/notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Note ID |
| `text` | body | `string` | no | New text content for the note |
| `icon` | body | `string` | no | New icon for the note |
| `color` | body | `string` | no | New hex color for the icon |
| `folderId` | body | `string` | no | New parent folder ID |
| `keepBreaks` | body | `boolean` | no | Preserve extra blank lines as empty paragraphs |
