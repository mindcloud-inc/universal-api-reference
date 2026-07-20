# Create List Entry with Zixflow

Creates a new list entry in Zixflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/list-entries/:listId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Create List Entry](https://docs.zixflow.com/api-reference/list-entries/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | List identifier. |
| `recordId` | body | `string` | yes | Record identifier to add to the list. |
| `data` | body | `object` | no | Additional list-entry data payload. |
