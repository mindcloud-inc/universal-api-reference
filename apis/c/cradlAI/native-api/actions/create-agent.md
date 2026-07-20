# Create Agent with Cradl AI

Creates a new agent in Cradl AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Create Agent](https://docs.cradl.ai/api-reference/post-agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | body | `object` | no | Metadata attached to the agent. |
| `name` | body | `string` | no | Name of the agent. |
| `description` | body | `string` | no | Description of the agent. |
| `resourceIds[]` | body | `array<string>` | no | Resources attached to the agent. |
