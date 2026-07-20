# Update Project with Zeplin

Updates an existing project in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Project](https://docs.zeplin.dev/reference/updateproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `name` | body | `string` | yes | New name for the project |
| `description` | body | `string` | yes | New description for the project |
| `workflow_status_id` | body | `string` | yes | Id of the new workflow status for the project |
| `linked_styleguide_id` | body | `string` | yes | The unique id of the styleguide to be linked. Set null to unlink the linked styleguide. |
