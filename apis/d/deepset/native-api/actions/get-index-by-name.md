# Get Index By Name with Deepset

Retrieves a Deepset index by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/indexes/:index_name`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Index By Name](https://docs.cloud.deepset.ai/docs/api/main/get-index-by-name-api-v-1-workspaces-workspace-name-indexes-index-name-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index_name` | path | `string` | yes | deepset index name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
