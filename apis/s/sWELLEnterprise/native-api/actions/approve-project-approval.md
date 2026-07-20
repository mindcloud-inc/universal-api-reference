# Approve Project Approval with SWELLEnterprise

Approves a project approval in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/projects/:project_id/approvals/:approval_id/approve`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Approve Project Approval](https://dashboard.swellsystem.com/docs#endpoints-POSTapi-v1-projects-projects--project_id--approvals--approval_id--approve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The ID of the project. |
| `approval_id` | path | `number` | yes | The ID of the approval. |
