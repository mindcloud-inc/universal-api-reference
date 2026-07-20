# Get Contact By Phone with Callbell

Retrieves a Callbell contact by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/phone/:number`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Get Contact By Phone](https://docs.callbell.eu/api/reference/contacts_api/get_contact_by_phone/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_uuid` | query | `string` | no | Channel UUID to scope the phone lookup. |
| `number` | path | `string` | yes | Phone number to search for. |
