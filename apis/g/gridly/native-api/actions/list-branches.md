# List Branches with Gridly

Finds branches in Gridly by grid ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/branches`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [List Branches](https://www.gridly.com/docs/api/#list-branches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gridId` | query | `string` | yes | The unique identifier of the grid whose branches you want to list. |
