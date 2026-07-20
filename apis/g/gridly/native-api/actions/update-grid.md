# Update Grid with Gridly

Updates an existing grid in Gridly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/grids/:id`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Update Grid](https://www.gridly.com/docs/api/#update-a-grid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the grid to update. |
| `name` | body | `string` | no | The new name for the grid. |
| `metadata` | body | `object` | no | A metadata object to update on the grid. |
