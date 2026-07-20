# List Project Variable Collections with Zeplin

Retrieves a list of project variable collections from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/variable_collections`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Variable Collections](https://docs.zeplin.dev/reference/getprojectvariablecollections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
