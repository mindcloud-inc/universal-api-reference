# Create View with Gridly

Creates a new view in Gridly.

## Endpoint

- **Method:** `POST`
- **Path:** `/views`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Create View](https://www.gridly.com/docs/api/#create-view)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the view to create. |
| `gridId` | body | `string` | yes | The unique identifier of the grid that the new view belongs to. |
| `columns[]` | body | `array<object>` | no | An optional list of existing columns to add to the view when creating it. |
