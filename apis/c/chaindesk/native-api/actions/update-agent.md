# Update Agent with Chaindesk

Updates an existing agent in Chaindesk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/agents/:agentId`
- **Base URL:** `https://app.chaindesk.ai/api`
- **Official documentation:** [Update Agent](https://docs.chaindesk.ai/api-reference/endpoint/agents/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | path | `string` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
