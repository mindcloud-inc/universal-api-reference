# Create Note with SureContact

Creates a new note for a SureContact contact.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/contacts/:contact_uuid/notes`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Create Note](https://api.surecontact.com/docs#contact-notes-POSTapi-v1-public-contacts--contact_uuid--notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_uuid` | path | `string` | yes | The UUID of the contact. |
| `content` | body | `string` | yes | The note content. |
| `title` | body | `string` | no | Optional title for the note. |
