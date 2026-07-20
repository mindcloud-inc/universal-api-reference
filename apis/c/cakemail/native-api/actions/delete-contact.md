# Delete Contact with Cakemail

Deletes a contact from a Cakemail list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/:listId/contacts/:contactId`
- **Base URL:** `https://api.cakemail.dev`
- **Official documentation:** [Delete Contact](https://cakemail.dev/en/api/contact#delete-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Cakemail list ID. |
| `contactId` | path | `number` | yes | Cakemail contact ID. |
