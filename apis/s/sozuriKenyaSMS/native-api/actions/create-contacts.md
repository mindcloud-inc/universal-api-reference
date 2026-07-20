# Create Contacts with Sozuri (Kenya) SMS

Creates one or more contacts in Sozuri.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Create Contacts](https://sozuri.net/docs/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | body | `string` | no | The group to add the contacts into. |
| `contacts[]` | body | `array<object>` | yes | The contacts to create. |
