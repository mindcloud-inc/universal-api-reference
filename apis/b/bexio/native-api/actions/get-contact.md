# Get Contact with Bexio

Retrieves a contact from Bexio.

## Endpoint

- **Method:** `GET`
- **Path:** `/2.0/contact/:contact_id`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Get Contact](https://docs.bexio.com/#tag/Contacts/operation/v2ShowContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The ID of the contact. |
| `show_archived` | query | `boolean` | no | Show archived elements only. |
