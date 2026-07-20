# Search Namespace with Agentset

Searches an Agentset namespace by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/search`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Search Namespace](https://docs.agentset.ai/api-reference/endpoint/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
| `query` | body | `string` | yes | The search query text. |
