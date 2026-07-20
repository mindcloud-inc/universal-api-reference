# List Contact Messages with Callbell

Retrieves messages for a specific Callbell contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:uuid/messages`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [List Contact Messages](https://docs.callbell.eu/api/reference/contacts_api/get_contact_messages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number of messages to retrieve. |
| `uuid` | path | `string` | yes | Unique identifier of the contact. |
