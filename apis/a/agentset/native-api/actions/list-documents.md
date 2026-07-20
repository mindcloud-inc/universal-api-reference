# List Documents with Agentset

Retrieves documents from an Agentset namespace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/namespace/:namespaceId/documents`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [List Documents](https://docs.agentset.ai/api-reference/endpoint/documents/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
