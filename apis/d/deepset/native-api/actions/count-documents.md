# Count Documents with Deepset

Retrieves the document count for a Deepset index.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/indexes/:index_name/documents/count`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Count Documents](https://docs.cloud.deepset.ai/docs/api/main/count-documents-api-v-1-workspaces-workspace-name-indexes-index-name-documents-count-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index_name` | path | `string` | yes | deepset index name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
