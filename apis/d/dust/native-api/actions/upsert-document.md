# Upsert Document with Dust

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/w/:workspaceId/spaces/:spaceId/data_sources/:dataSourceId/documents`
- **Base URL:** `https://dust.tt`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataSourceId` | path | `string` | yes | Dust data source sId. |
| `document_id` | body | `string` | yes | Stable external ID for the document. |
| `spaceId` | path | `string` | yes | Dust space sId. |
| `text` | body | `string` | yes | Plain text document content. |
| `title` | body | `string` | yes | Document title. |
