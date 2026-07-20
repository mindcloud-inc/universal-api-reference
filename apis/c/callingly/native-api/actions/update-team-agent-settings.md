# Update Team Agent Settings with Callingly

Updates team agent settings in Callingly.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/teams/{{id}}/agents/{{agent_id}}`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Update Team Agent Settings](https://help.callingly.com/article/38-callingly-api-documentation#update-agent-settings)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cap` | body | `string` | no |
| `id` | path | `string` | yes |
| `priority` | body | `string` | no |
| `agent_id` | path | `string` | yes |
