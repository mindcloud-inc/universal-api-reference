# List Workspace Files with Browser Use

Retrieves workspace files from Browser Use.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspace_id/files`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [List Workspace Files](https://docs.browser-use.com/cloud/api-v3/workspaces/list-workspace-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor. |
| `includeUrls` | query | `boolean` | no | Whether to include presigned download URLs. |
| `limit` | query | `number` | no | Maximum number of files to return. |
| `prefix` | query | `string` | no | Directory prefix to list. |
| `shallow` | query | `boolean` | no | Whether to list only immediate children. |
| `workspace_id` | path | `string` | yes | Workspace ID. |
