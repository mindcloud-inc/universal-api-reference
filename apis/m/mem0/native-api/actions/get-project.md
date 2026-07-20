# Get Project with Mem0

Retrieves a project from Mem0.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/orgs/organizations/:org_id/projects/:project_id/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [Get Project](https://docs.mem0.ai/api-reference/project/get-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Mem0 organization ID from the project resource path. |
| `project_id` | path | `string` | yes | Mem0 project ID from the project resource path. |
