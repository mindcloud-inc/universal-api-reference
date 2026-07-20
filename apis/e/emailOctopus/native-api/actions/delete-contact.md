# Delete Contact with EmailOctopus

Deletes a contact from an EmailOctopus list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/:listId/contacts/:memberId`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [Delete Contact](https://emailoctopus.com/api-documentation/lists/delete-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | The unique ID of the list. |
| `memberId` | path | `string` | yes | The unique ID of the contact. |
