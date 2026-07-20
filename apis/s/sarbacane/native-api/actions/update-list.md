# Update List with Sarbacane

Updates an existing list in Sarbacane.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/{listId}`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Update List](https://developers.sarbacane.com/contacts/#edit-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | no | Sarbacane list ID. |
| `name` | body | `string` | no | Updated list name. |
