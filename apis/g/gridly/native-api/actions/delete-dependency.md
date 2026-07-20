# Delete Dependency with Gridly

Deletes an existing dependency from a Gridly view.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/views/:viewId/dependencies/:id`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Delete Dependency](https://www.gridly.com/docs/api/#delete-a-dependency)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view that contains the dependency. |
| `id` | path | `string` | yes | The unique identifier of the dependency to delete. |
