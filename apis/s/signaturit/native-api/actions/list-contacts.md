# List Contacts with Signaturit

Retrieves contacts from Signaturit.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [List Contacts](https://docs.signaturit.com/api/latest#contacts_get_contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of contacts to return. |
| `offset` | query | `number` | no | Results offset. |
| `email` | query | `string` | no | Filter contacts by email. |
| `name` | query | `string` | no | Filter contacts by name. |
