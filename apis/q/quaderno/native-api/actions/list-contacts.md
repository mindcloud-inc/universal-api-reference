# List Contacts with Quaderno

Retrieves contact records from Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [List Contacts](https://developers.quaderno.io/api/#tag/Contacts/operation/listContacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `processor_id` | query | `string` | no | Filter contacts by processor ID. |
| `q` | query | `string` | no | Filter contacts by full name, email, or tax ID. |
