# Get Column with Gridly

Retrieves a column from Gridly by column ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/views/:viewId/columns/:id`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Get Column](https://www.gridly.com/docs/api/#retrieve-a-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view that contains the column. |
| `id` | path | `string` | yes | The unique identifier of the column to retrieve. |
