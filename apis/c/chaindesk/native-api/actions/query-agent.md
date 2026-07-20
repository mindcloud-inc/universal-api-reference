# Query Agent with Chaindesk

Sends a query to an agent in Chaindesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/:agentId/query`
- **Base URL:** `https://app.chaindesk.ai/api`
- **Official documentation:** [Query Agent](https://docs.chaindesk.ai/api-reference/endpoint/agents/query)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | path | `string` | yes |
| `query` | body | `string` | yes |
