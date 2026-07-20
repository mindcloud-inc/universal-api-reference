# Create Note with Peach

Creates a note for a contact in Peach.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Create Note](https://peach-organization.gitbook.io/peach/api-reference/interactions/create-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | body | `string` | yes | The contact ID that should receive the note. |
| `noteTitle` | body | `string` | no | Optional title for the note. |
| `noteBody` | body | `string` | yes | The note content. |
