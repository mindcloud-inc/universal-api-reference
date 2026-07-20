# Remove Team Agent with Callingly

Deletes a team agent from Callingly.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/teams/{{id}}/agents/{{agent_id}}`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Remove Team Agent](https://help.callingly.com/article/38-callingly-api-documentation#remove-agents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `agent_id` | path | `string` | yes |
