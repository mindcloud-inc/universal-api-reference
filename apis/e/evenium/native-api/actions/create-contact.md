# Create Contact with Evenium

Creates a new contact in Evenium.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://evenium.com/api/1`
- **Official documentation:** [Create Contact](https://static.evenium.com/api-docs/organizer/index-json.html#_create_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | The Evenium Company. |
| `customId` | body | `string` | yes | The Evenium Custom ID. |
| `email` | body | `string` | yes | The Evenium Email. |
| `firstName` | body | `string` | yes | The Evenium First Name. |
| `lastName` | body | `string` | yes | The Evenium Last Name. |
