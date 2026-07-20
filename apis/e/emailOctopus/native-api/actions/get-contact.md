# Get Contact with EmailOctopus

Retrieves a contact from EmailOctopus by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/contacts/:memberId`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [Get Contact](https://emailoctopus.com/api-documentation/lists/get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | The unique ID of the list. |
| `memberId` | path | `string` | yes | The unique ID of the contact. |
