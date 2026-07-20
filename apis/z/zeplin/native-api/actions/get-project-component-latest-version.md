# Get Project Component Latest Version with Zeplin

Retrieves the latest project component version from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/components/{component_id}/versions/latest`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Project Component Latest Version](https://docs.zeplin.dev/reference/getprojectcomponentlatestversion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `component_id` | path | `string` | yes | Component id |
| `include_linked_styleguides` | query | `boolean` | no | Whether to include linked styleguides or not |
