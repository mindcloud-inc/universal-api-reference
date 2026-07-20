# Update Note with SureContact

Updates an existing note in SureContact.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/v1/public/notes/:note_uuid`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Update Note](https://api.surecontact.com/docs#contact-notes-PUTapi-v1-public-notes--note_uuid-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | The updated note content. |
| `note_uuid` | path | `string` | yes | The UUID of the note. |
| `title` | body | `string` | no | Optional title for the note. |
