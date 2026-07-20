# Update Agent with Cradl AI

Updates an existing agent in Cradl AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agents/:agentId`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Update Agent](https://docs.cradl.ai/api-reference/patch-agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Identifier of the agent to update. |
| `metadata` | body | `object` | no | Metadata attached to the agent. |
| `name` | body | `string` | no | Updated agent name. |
| `description` | body | `string` | no | Updated agent description. |
| `resourceIds[]` | body | `array<string>` | no | Updated resources attached to the agent. |
