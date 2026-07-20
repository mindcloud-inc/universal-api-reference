# Update Contact with Heyy

Updates an existing contact in Heyy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Update Contact](https://docs.heyy.io/api-reference/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Heyy contact ID. |
| `firstName` | body | `string` | no | The contact first name. |
| `lastName` | body | `string` | no | The contact last name. |
