# Create Note with Attio

Creates a note in Attio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/notes`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Create Note](https://docs.attio.com/rest-api/endpoint-reference/notes/create-a-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentObject` | body | `string` | yes | The ID or slug of the parent object the note belongs to. |
| `parentRecordId` | body | `string` | yes | The ID of the parent record the note belongs to. |
| `title` | body | `string` | yes | The note title. The title is plaintext only and has no formatting. |
| `format` | body | `list<string>` | no | Specify the format for the note content. Defaults to plaintext; choose markdown for rich formatting. Accepted values: `markdown`, `plaintext`. |
| `content` | body | `string` | yes | The main content of the note, formatted according to the format field. |
| `createdAt` | body | `date` | no | Optional backdated created-at timestamp in ISO 8601 format. |
| `meetingId` | body | `string` | no | Optional meeting to associate with the note. |
