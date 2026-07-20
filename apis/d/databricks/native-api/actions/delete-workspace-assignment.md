# Delete Workspace Assignment with Databricks

Deletes a workspace assignment from Databricks.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/2.0/accounts/{accountId}/workspaces/:workspaceId/permissionassignments/principals/:principalId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Delete Workspace Assignment](https://docs.databricks.com/api/account/workspaceassignment/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | The workspace ID for the account. |
| `principal_id` | path | `number` | yes | The ID of the user, service principal, or group. |
