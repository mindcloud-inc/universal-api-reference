# Get Suppression List Contact with Postalytics

Retrieves a Postalytics suppression-list contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/lists/suppression/contacts/:listId/:contactId`
- **Base URL:** `https://api.postalytics.com`
- **Official documentation:** [Get Suppression List Contact](https://docs.postalytics.com/references/postalytics-rest-api/get-suppression-list-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Suppression list ID. |
| `contactId` | path | `number` | yes | Suppression contact ID. |
| `offset` | query | `number` | no | Starting offset. |
