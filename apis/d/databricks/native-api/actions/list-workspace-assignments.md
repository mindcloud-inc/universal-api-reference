# List Workspace Assignments with Databricks

Retrieves workspace assignments from Databricks for a workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/accounts/{accountId}/workspaces/:workspaceId/permissionassignments`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List Workspace Assignments](https://docs.databricks.com/api/account/workspaceassignment/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | The workspace ID for the account. |
