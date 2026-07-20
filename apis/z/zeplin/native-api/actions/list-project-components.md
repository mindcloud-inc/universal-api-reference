# List Project Components with Zeplin

Retrieves a list of project components from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/components`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Components](https://docs.zeplin.dev/reference/getprojectcomponents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `section_id` | query | `string` | no | Filter by section id |
| `sort` | query | `string` | no | Sort components by their `section` or their `created` date |
| `include_latest_version` | query | `boolean` | no | Whether to include the latest version data in the Component object |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
