# List AI Agents with Make

Lists AI agents for the specified team.

## Endpoint

- **Method:** `GET`
- **Path:** `/ai-agents/v1/agents`
- **Base URL:** `https://us2.make.com/api/v2`
- **Official documentation:** [List AI Agents](https://developers.make.com/api-documentation/api-reference/ai-agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `number` | yes | The ID of the Make team whose AI agents should be listed. |
