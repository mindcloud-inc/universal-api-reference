# List Files with Deepset

Retrieves files from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/files`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [List Files](https://docs.cloud.deepset.ai/docs/api/main/list-files-api-v-1-workspaces-workspace-name-files-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
