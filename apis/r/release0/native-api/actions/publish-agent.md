# Publish Agent with Release0

Publishes an agent for public access in Release0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/:agentId/publish`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Publish Agent](https://docs.release0.com/api-reference/agent/publish)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The agent ID to publish. |
