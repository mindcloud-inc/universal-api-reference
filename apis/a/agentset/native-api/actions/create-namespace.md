# Create Namespace with Agentset

Creates a new namespace in Agentset.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/namespace`
- **Base URL:** `https://api.agentset.ai`
- **Official documentation:** [Create Namespace](https://docs.agentset.ai/api-reference/endpoint/namespaces/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The namespace name. |
| `slug` | body | `string` | yes | A URL-safe namespace slug. |
