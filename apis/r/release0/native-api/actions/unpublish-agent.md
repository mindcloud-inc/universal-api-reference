# Unpublish Agent with Release0

Unpublishes an agent from public access in Release0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/:agentId/unpublish`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Unpublish Agent](https://docs.release0.com/api-reference/agent/unpublish)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The agent ID to unpublish. |
