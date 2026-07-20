# Get Search Sessions with Deepset

Retrieves search sessions from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/search_sessions`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Search Sessions](https://docs.cloud.deepset.ai/docs/api/main/get-search-sessions-api-v-1-workspaces-workspace-name-search-sessions-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
