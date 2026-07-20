# Update Agent with Release0

Updates an agent in Release0.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/agents/:agentId`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Update Agent](https://docs.release0.com/api-reference/agent/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The agent identifier to update. |
| `agent` | body | `object` | yes | The partial or full agent payload to persist. |
