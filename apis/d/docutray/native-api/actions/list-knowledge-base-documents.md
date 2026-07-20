# List Knowledge Base Documents with Docutray

## Endpoint

- **Method:** `GET`
- **Path:** `api/knowledge-bases/:id/documents`
- **Base URL:** `https://app.docutray.com`
- **Official documentation:** [List Knowledge Base Documents](https://docs.docutray.com/docs/operations/knowledge-bases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | query | `string` | no | Filter by document ID |
| `id` | path | `string` | yes | Unique ID of the Knowledge Base |
| `search` | query | `string` | no | Search in documents |
