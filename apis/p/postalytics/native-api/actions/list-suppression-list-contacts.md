# List Suppression List Contacts with Postalytics

Retrieves contacts on a Postalytics suppression list.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/lists/suppression/contacts/:listId`
- **Base URL:** `https://api.postalytics.com`
- **Official documentation:** [List Suppression List Contacts](https://docs.postalytics.com/references/postalytics-rest-api/get-suppression-list-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `number` | yes | Suppression list ID. |
| `offset` | query | `number` | no | Starting offset. |
