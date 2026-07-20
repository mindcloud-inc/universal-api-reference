# Create Dependency with Gridly

Creates a new dependency in a Gridly view.

## Endpoint

- **Method:** `POST`
- **Path:** `/views/:viewId/dependencies`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [Create Dependency](https://www.gridly.com/docs/api/#create-a-dependency)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view where the dependency should be created. |
| `sourceColumnId` | body | `string` | yes | The source column ID for the dependency. |
| `targetColumnId` | body | `string` | yes | The target column ID for the dependency. |
