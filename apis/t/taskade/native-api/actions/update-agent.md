# Update Agent with Taskade

Updates an existing agent in Taskade.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agents/:agentId`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [Update Agent](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/agents/update-agent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | Agent ID. |
| `name` | body | `string` | yes | Agent name. |
| `data.commands[].name` | body | `string` | yes | Single command display name. |
| `data.commands[].prompt` | body | `string` | yes | Single command prompt text. |
| `data.description` | body | `string` | yes | Agent description. |
| `data.avatar.data.value` | body | `string` | yes | Avatar emoji value. |
