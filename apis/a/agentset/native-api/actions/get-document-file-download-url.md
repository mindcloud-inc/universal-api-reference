# Get Document File Download URL with Agentset

Retrieves a presigned download URL for a source file from Agentset.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/documents/:documentId/file-download-url`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Get Document File Download URL](https://docs.agentset.ai/api-reference/endpoint/documents/file-download-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The document ID. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
