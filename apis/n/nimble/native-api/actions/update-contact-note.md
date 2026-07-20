# Update Contact Note with Nimble

Updates an existing note for Nimble contacts.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/contacts/notes/:note_id`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Update Contact Note](https://www.nimble.com/developers/docs/#tag/Contacts/operation/put-contact-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note_id` | path | `string` | yes | Nimble note_id path parameter. |
| `contact_ids[]` | body | `array<string>` | yes | — |
| `note` | body | `string` | yes | — |
| `note_preview` | body | `string` | yes | — |
