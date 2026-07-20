# List Grids with Gridly

Finds grids in Gridly by database ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/grids`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [List Grids](https://www.gridly.com/docs/api/#list-grids)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dbId` | query | `string` | yes | The unique identifier of the database whose grids you want to list. |
