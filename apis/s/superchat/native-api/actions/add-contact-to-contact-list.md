# Add Contact to Contact List with Superchat

Adds a contact to a Superchat contact list.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/{contact_id}/contact-lists`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [Add Contact to Contact List](https://developers.superchat.com/reference/createcontactlistsforcontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact |
| `id` | body | `string` | no | Unique identifier of the contact list. Always bears prefix 'cl_' |
