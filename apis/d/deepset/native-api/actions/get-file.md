# Get File with Deepset

Retrieves a file from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/files/:file_id`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get File](https://docs.cloud.deepset.ai/docs/api/main/get-file-api-v-1-workspaces-workspace-name-files-file-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | deepset file ID. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
