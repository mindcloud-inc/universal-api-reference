# Search Agent Knowledgebase with echowin

Finds knowledge base entries in echowin by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/:agentId/knowledgebase/search`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Search Agent Knowledgebase](https://echo.win/api-docs/knowledgebase#agent-search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | path | `string` | yes |
| `query` | query | `string` | yes |
| `limit` | query | `number` | no |
| `threshold` | query | `number` | no |
