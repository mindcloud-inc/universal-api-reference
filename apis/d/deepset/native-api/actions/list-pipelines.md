# List Pipelines with Deepset

Retrieves pipelines from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [List Pipelines](https://docs.cloud.deepset.ai/docs/api/main/list-pipelines-api-v-1-workspaces-workspace-name-pipelines-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
