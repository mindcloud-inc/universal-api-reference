# List Agent Tasks with Relevance AI

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/conversations/list`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [List Agent Tasks](https://sdk.relevanceai.com/concepts/tasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | query | `string` | yes |
| `pageSize` | query | `number` | no |
| `search` | query | `string` | no |
| `status` | query | `string` | no |
