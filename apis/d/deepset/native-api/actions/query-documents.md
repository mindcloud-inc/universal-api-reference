# Query Documents with Deepset

Queries documents in a Deepset index.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspaces/:workspace_name/indexes/:index_name/documents-query`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Query Documents](https://docs.cloud.deepset.ai/docs/api/main/query-documents-api-v-1-workspaces-workspace-name-indexes-index-name-documents-query-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `index_name` | path | `string` | yes | deepset index name. |
| `query` | body | `string` | yes | Document query payload. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
