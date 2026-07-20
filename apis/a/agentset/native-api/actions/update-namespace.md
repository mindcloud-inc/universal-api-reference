# Update Namespace with Agentset

Updates an existing namespace in Agentset.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/namespace/:namespaceId`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Update Namespace](https://docs.agentset.ai/api-reference/endpoint/namespaces/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The updated namespace name. |
| `namespaceId` | path | `string` | yes | The Agentset namespace ID, prefixed with ns_. |
| `slug` | body | `string` | no | The updated namespace slug. |
