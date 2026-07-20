# Update Note with Lunatask

## Endpoint

- **Method:** `PUT`
- **Path:** `/notes/:id`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Update Note](https://lunatask.app/api/notes-api/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the note to update |
| `name` | body | `string` | no | The updated note name |
| `content` | body | `string` | no | The updated note content in Markdown |
| `notebook_id` | body | `string` | no | The notebook ID for the note |
| `date_on` | body | `date` | no | The ISO-8601 formatted date assigned to the note |
