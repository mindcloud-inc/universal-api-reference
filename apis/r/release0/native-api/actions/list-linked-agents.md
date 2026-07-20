# List Linked Agents with Release0

Retrieves agents linked to a Release0 agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/agents/:agentId/linkedAgents`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [List Linked Agents](https://docs.release0.com/editor/elements/logic/link-to-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The agent ID. |
