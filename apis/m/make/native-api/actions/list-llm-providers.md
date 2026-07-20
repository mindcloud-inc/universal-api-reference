# List LLM Providers with Make

Lists LLM providers for the specified team.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai-agents/v1/llm-providers`
- **Base URL:** `https://us2.make.com/api/v2`
- **Official documentation:** [List LLM Providers](https://developers.make.com/api-documentation/api-reference/ai-agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `number` | yes | The ID of the Make team whose LLM providers should be listed. |
