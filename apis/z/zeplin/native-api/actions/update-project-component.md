# Update Project Component with Zeplin

Updates an existing project component in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/components/{component_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Project Component](https://docs.zeplin.dev/reference/updateprojectcomponent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `component_id` | path | `string` | yes | Component id |
| `description` | body | `string` | yes | New description for component |
