# Update List with EmailOctopus

Updates an existing list in EmailOctopus.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId`
- **Base URL:** `https://emailoctopus.com/api/1.6`
- **Official documentation:** [Update List](https://emailoctopus.com/api-documentation/lists/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | The unique ID of the list. |
| `name` | query | `string` | yes | The new name of the list. |
