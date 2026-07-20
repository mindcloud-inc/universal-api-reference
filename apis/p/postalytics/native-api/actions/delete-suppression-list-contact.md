# Delete Suppression List Contact with Postalytics

Deletes a contact from a Postalytics suppression list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/lists/suppression/contacts/:listId/:contactId`
- **Base URL:** `https://api.postalytics.com`
- **Official documentation:** [Delete Suppression List Contact](https://docs.postalytics.com/references/postalytics-rest-api/delete-suppression-list-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Suppression list ID. |
| `contactId` | path | `number` | yes | Suppression contact ID. |
