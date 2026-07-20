# Get Document with Deepset

Retrieves a document from a Deepset index.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/indexes/:index_name/documents/:document_id`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Document](https://docs.cloud.deepset.ai/docs/api/main/get-document-api-v-1-workspaces-workspace-name-indexes-index-name-documents-document-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | deepset document ID. |
| `index_name` | path | `string` | yes | deepset index name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
