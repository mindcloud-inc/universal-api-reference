# Get Dependency with Gridly

Retrieves a dependency from Gridly by dependency ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/views/:viewId/dependencies/:id`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Get Dependency](https://www.gridly.com/docs/api/#retrieve-a-dependency)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view that contains the dependency. |
| `id` | path | `string` | yes | The unique identifier of the dependency to retrieve. |
