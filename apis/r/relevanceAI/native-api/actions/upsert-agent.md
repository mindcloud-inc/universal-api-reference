# Upsert Agent with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/upsert`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Upsert Agent](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent_id` | body | `string` | no |
| `model` | body | `string` | no |
| `name` | body | `string` | no |
| `system_prompt` | body | `string` | no |
| `temperature` | body | `number` | no |
