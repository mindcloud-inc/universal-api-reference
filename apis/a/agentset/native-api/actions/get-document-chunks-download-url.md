# Get Document Chunks Download URL with Agentset

Retrieves a presigned download URL for document chunks from Agentset.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/documents/:documentId/chunks-download-url`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Get Document Chunks Download URL](https://docs.agentset.ai/api-reference/endpoint/documents/chunks-download-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The document ID. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
