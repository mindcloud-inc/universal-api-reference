# Add Tool to Agent with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/upsert`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Add Tool to Agent](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | body | `string` | yes |
| `existingActions` | body | `object` | yes |
| `toolId` | body | `string` | yes |
