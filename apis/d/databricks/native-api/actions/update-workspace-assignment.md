# Update Workspace Assignment with Databricks

Updates a workspace assignment in Databricks.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/2.0/accounts/{accountId}/workspaces/:workspaceId/permissionassignments/principals/:principalId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Update Workspace Assignment](https://docs.databricks.com/api/account/workspaceassignment/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | The workspace ID. |
| `principal_id` | path | `number` | yes | The ID of the user, service principal, or group. |
| `permissions` | body | `list<string>` | yes | Array of permissions assignments to update on the workspace. Valid values are "USER" and "ADMIN" (case-sensitive). If both "USER" and "ADMIN" are provided, "ADMIN" takes precedence. Other values will be ignored. Note that excluding this field, or providing unsupported values, will have the same effect as providing an empty list, which will result in the deletion of all permissions for the principal. |
