# Update Contact with Channels

Updates an existing contact in Channels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/{contactId}`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [Update Contact](https://developers.channels.app/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Contact ID to update. |
| `firstName` | body | `string` | no | Updated first name for the contact. |
| `lastName` | body | `string` | no | Updated last name for the contact. |
| `company` | body | `string` | no | Updated company for the contact. |
| `email` | body | `string` | no | Updated email for the contact. |
