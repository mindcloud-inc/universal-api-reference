# List Indexes with Deepset

Retrieves indexes from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/indexes`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [List Indexes](https://docs.cloud.deepset.ai/docs/api/main/get-indexes-api-v-1-workspaces-workspace-name-indexes-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
