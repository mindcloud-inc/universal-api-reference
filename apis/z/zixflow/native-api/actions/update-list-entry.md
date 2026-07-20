# Update List Entry with Zixflow

Updates an existing list entry in Zixflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/list-entries/:listId/:entryId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Update List Entry](https://docs.zixflow.com/api-reference/list-entries/edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | List identifier. |
| `entryId` | path | `string` | yes | List entry identifier. |
| `data` | body | `object` | no | List-entry update payload. |
