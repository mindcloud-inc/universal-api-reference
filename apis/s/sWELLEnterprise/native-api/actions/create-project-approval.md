# Create Project Approval with SWELLEnterprise

Creates a project approval in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/projects/:project_id/approvals`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Create Project Approval](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--approvals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The ID of the project. |
| `type` | body | `string` | yes | Approval type. Runtime evidence verified final for this account. |
