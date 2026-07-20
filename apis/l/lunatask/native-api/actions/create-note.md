# Create Note with Lunatask

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://api.lunatask.app/v1`
- **Official documentation:** [Create Note](https://lunatask.app/api/notes-api/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notebook_id` | body | `string` | no | The Notebook ID of the notebook where the note should be created |
| `name` | body | `string` | no | The name of the note |
| `content` | body | `string` | no | The content of the note in Markdown |
| `date_on` | body | `date` | no | A date assigned to the note |
| `source` | body | `string` | no | Identification of the external system where the note is coming from |
| `source_id` | body | `string` | no | The ID of the record in the external system |
