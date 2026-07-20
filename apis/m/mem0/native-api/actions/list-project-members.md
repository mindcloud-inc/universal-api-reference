# List Project Members with Mem0

Retrieves project members from Mem0.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/orgs/organizations/:org_id/projects/:project_id/members/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [List Project Members](https://docs.mem0.ai/api-reference/project/get-project-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Mem0 organization ID from the project member resource path. |
| `project_id` | path | `string` | yes | Mem0 project ID from the project member resource path. |
