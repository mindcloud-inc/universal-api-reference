# Warm Namespace Cache with Agentset

Starts a namespace cache warm-up in Agentset.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/warm-up`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Warm Namespace Cache](https://docs.agentset.ai/api-reference/endpoint/namespaces/warm-up)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
