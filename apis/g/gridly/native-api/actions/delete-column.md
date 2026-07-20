# Delete Column with Gridly

Deletes an existing column from a Gridly view.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/views/:viewId/columns/:id`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Delete Column](https://www.gridly.com/docs/api/#delete-a-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view that contains the column. |
| `id` | path | `string` | yes | The unique identifier of the column to delete. |
