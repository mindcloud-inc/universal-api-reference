# List Screen Components with Zeplin

Retrieves a list of screen components from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/screens/{screen_id}/components`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Screen Components](https://docs.zeplin.dev/reference/getscreencomponents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `include_latest_version` | query | `boolean` | no | Whether to include the latest version data in the Component object |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
