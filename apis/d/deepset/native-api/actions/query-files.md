# Query Files with Deepset

Queries files in a Deepset workspace with SQL.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspaces/:workspace_name/files/_sql`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Query Files](https://docs.cloud.deepset.ai/docs/api/main/query-files-api-v-1-workspaces-workspace-name-files-sql-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | SQL query for files. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
