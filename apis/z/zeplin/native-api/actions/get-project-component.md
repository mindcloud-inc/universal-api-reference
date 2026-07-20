# Get Project Component with Zeplin

Retrieves a project component from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/components/{component_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Project Component](https://docs.zeplin.dev/reference/getprojectcomponent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `component_id` | path | `string` | yes | Component id |
| `include_latest_version` | query | `boolean` | no | Whether to include the latest version data in the Component object |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
