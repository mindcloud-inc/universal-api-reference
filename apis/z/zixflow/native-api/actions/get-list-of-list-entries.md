# Get List of List Entries with Zixflow

Retrieves list entries from Zixflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/list-entries/:listId/query`
- **Base URL:** `https://api.zixflow.com/api/v1`
- **Official documentation:** [Get List of List Entries](https://docs.zixflow.com/api-reference/list-entries/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listId` | path | `string` | yes | List identifier. |
| `filter` | body | `object` | no | Filter object for list-entry query. |
| `sort[]` | body | `array` | no | Sort instructions for list-entry query. |
| `limit` | body | `number` | no | Maximum number of entries to return. |
| `offset` | body | `number` | no | Number of entries to skip. |
