# List Dependencies with Gridly

Finds dependencies in a specific Gridly view.

## Endpoint

- **Method:** `GET`
- **Path:** `/views/:viewId/dependencies`
- **Base URL:** `https://api.gridly.com/v1`
- **Official documentation:** [List Dependencies](https://www.gridly.com/docs/api/#list-dependencies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `viewId` | path | `string` | yes | The unique identifier of the view whose dependencies you want to list. |
