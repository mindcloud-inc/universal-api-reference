# List Web Tools with Hamsa

Retrieves available web tools from Hamsa.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/voice-agents/web-tool/list`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [List Web Tools](https://docs.tryhamsa.com/api-reference/endpoint/v2/list-web-tools)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `collectionId` | query | `string` | no |
| `isActive` | query | `string` | no |
| `returnUncategorized` | query | `string` | no |
| `search` | query | `string` | no |
| `skip` | query | `number` | no |
| `take` | query | `number` | no |
| `type` | query | `string` | no |
| `voiceAgentId` | query | `string` | no |
