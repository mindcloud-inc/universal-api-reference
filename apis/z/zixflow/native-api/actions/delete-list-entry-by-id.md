# Delete List Entry By ID with Zixflow

Deletes an existing list entry from Zixflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/list-entries/:listId/:entryId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Delete List Entry By ID](https://docs.zixflow.com/api-reference/list-entries/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | List identifier. |
| `entryId` | path | `string` | yes | List entry identifier. |
