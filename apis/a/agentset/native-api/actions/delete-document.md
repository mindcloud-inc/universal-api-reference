# Delete Document with Agentset

Deletes a document from Agentset.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/namespace/:namespaceId/documents/:documentId`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Delete Document](https://docs.agentset.ai/api-reference/endpoint/documents/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The document ID. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
