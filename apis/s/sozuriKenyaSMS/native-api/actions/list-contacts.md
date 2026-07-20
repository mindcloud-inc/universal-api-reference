# List Contacts with Sozuri (Kenya) SMS

Retrieves contacts from Sozuri.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [List Contacts](https://sozuri.net/docs/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | query | `string` | no | The group name to fetch contacts from. If omitted, all contacts are returned. |
