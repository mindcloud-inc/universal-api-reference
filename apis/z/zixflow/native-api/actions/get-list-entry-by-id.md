# Get List Entry By ID with Zixflow

Retrieves a list entry from Zixflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/list-entries/:listId/:entryId`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get List Entry By ID](https://docs.zixflow.com/api-reference/list-entries/get-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | List identifier. |
| `entryId` | path | `string` | yes | List entry identifier. |
