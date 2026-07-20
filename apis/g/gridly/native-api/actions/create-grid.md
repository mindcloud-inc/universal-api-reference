# Create Grid with Gridly

Creates a new grid in Gridly.

## Endpoint

- **Method:** `POST`
- **Path:** `/grids`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Create Grid](https://www.gridly.com/docs/api/#create-grid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dbId` | query | `string` | yes | The unique identifier of the database where the grid should be created. |
| `name` | body | `string` | no | The name of the grid to create. |
| `templateGridId` | body | `string` | no | An existing Gridly template grid ID to create from. |
| `metadata` | body | `object` | no | A metadata object to store with the grid. |
