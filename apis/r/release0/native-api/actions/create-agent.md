# Create Agent with Release0

Creates a new agent in Release0.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Create Agent](https://docs.release0.com/api-reference/agent/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | body | `object` | no | Optional agent payload object for draft creation. |
| `workspaceId` | body | `string` | yes | The workspace ID that will own the new agent. |
