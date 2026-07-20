# List Views with Gridly

Finds views in Gridly by grid or branch.

## Endpoint

- **Method:** `GET`
- **Path:** `/views`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [List Views](https://www.gridly.com/docs/api/#list-views)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gridId` | query | `string` | no | The unique identifier of the grid whose views you want to list. |
| `branchId` | query | `string` | no | The unique identifier of the branch whose views you want to list when you are not listing by grid. |
