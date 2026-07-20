# List Project Connected Components with Zeplin

Retrieves a list of project connected components from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/connected_components`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Connected Components](https://docs.zeplin.dev/reference/getprojectconnectedcomponents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
