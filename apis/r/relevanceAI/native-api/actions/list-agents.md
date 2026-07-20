# List Agents with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/list`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [List Agents](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | body | `number` | no | Maximum number of agents to return. The official SDK defaults to 20 when omitted. |
| `page` | body | `number` | no | Page number to return. The official SDK defaults to 1 when omitted. |
