# Retrieve Hosting Configuration with Agentset

Retrieves hosting configuration from Agentset.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/namespace/:namespaceId/hosting`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Retrieve Hosting Configuration](https://docs.agentset.ai/api-reference/endpoint/hosting/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
