# Retrieve Document with Agentset

Retrieves a document from Agentset by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/namespace/:namespaceId/documents/:documentId`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Retrieve Document](https://docs.agentset.ai/api-reference/endpoint/documents/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentId` | path | `string` | yes | The document ID. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
