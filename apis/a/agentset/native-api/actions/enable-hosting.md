# Enable Hosting with Agentset

Enables hosting for an Agentset namespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace/:namespaceId/hosting`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Enable Hosting](https://docs.agentset.ai/api-reference/endpoint/hosting/enable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
