# List Contacts by Tag with EmailOctopus

Retrieves contacts from an EmailOctopus list by tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:listId/tags/:listTag/contacts`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [List Contacts by Tag](https://emailoctopus.com/api-documentation/lists/get-tagged)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | The unique ID of the list. |
| `listTag` | path | `string` | yes | The tag value used to filter list contacts. |
