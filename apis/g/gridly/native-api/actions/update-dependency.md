# Update Dependency with Gridly

Updates an existing dependency in a Gridly view.

## Endpoint

- **Method:** `PUT`
- **Path:** `/views/:viewId/dependencies/:id`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Update Dependency](https://www.gridly.com/docs/api/#update-a-dependency)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view that contains the dependency. |
| `id` | path | `string` | yes | The unique identifier of the dependency to update. |
| `sourceColumnId` | body | `string` | no | The updated source column ID for the dependency. |
| `targetColumnId` | body | `string` | no | The updated target column ID for the dependency. |
