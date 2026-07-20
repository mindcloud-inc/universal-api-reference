# List Contact Notes with Nimble

Retrieves notes for a contact from Nimble.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/contact/:contact_id/notes`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [List Contact Notes](https://www.nimble.com/developers/docs/#tag/Contacts/operation/list-contact-notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Nimble contact_id path parameter. |
