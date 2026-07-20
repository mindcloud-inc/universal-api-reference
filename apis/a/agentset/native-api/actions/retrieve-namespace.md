# Retrieve Namespace with Agentset

Retrieves a namespace from Agentset by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/namespace/:namespaceId`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Retrieve Namespace](https://docs.agentset.ai/api-reference/endpoint/namespaces/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
