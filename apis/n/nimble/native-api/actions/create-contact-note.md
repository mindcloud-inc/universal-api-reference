# Create Contact Note with Nimble

Creates a note for one or more Nimble contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/notes`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Create Contact Note](https://www.nimble.com/developers/docs/#tag/Contacts/operation/post-contact-note)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_ids[]` | body | `array<string>` | yes |
| `note` | body | `string` | yes |
| `note_preview` | body | `string` | yes |
