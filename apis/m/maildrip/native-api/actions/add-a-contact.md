# Add a contact with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Add a contact](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | query | `string` | no | ID of the group to add the contact to |
| `email` | body | `string` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
