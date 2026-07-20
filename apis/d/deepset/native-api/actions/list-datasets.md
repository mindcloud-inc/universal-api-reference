# List Datasets with Deepset

Retrieves datasets from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/datasets`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [List Datasets](https://docs.cloud.deepset.ai/docs/api/main/list-datasets-api-v-1-workspaces-workspace-name-datasets-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
