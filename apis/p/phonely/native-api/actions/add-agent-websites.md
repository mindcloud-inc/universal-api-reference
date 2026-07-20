# Add Agent Websites with Phonely

Adds websites to a Phonely agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/agent-websites`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Add Agent Websites](https://docs.phonely.ai/api-reference/endpoint/post-agent-websites)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `uid` | body | `string` | yes |
| `agentId` | body | `string` | yes |
| `url` | body | `string` | yes |
