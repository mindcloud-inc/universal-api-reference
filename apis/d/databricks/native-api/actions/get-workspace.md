# Get Workspace with Databricks

Retrieves a workspace from the Databricks account.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/2.0/accounts/{accountId}/workspaces/:workspaceId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Workspace](https://docs.databricks.com/api/account/workspaces/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes |
