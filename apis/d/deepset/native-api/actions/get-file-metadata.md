# Get File Metadata with Deepset

Retrieves metadata for a file in Deepset.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/files/:file_id/meta`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get File Metadata](https://docs.cloud.deepset.ai/docs/api/main/get-file-meta-api-v-1-workspaces-workspace-name-files-file-id-meta-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | deepset file ID. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
