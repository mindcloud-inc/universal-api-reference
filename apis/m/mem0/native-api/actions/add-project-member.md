# Add Project Member with Mem0

Adds a member to a project in Mem0.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/orgs/organizations/:org_id/projects/:project_id/members/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [Add Project Member](https://docs.mem0.ai/api-reference/project/add-project-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Mem0 organization ID from the project member resource path. |
| `project_id` | path | `string` | yes | Mem0 project ID from the project member resource path. |
