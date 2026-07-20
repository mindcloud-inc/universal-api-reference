# Delete Project with Mem0

Deletes a project from Mem0.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/orgs/organizations/:org_id/projects/:project_id/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [Delete Project](https://docs.mem0.ai/api-reference/project/delete-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Mem0 organization ID from the project resource path. |
| `project_id` | path | `string` | yes | Mem0 project ID from the project resource path. |
