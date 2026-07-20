# List Voice Agents with Hamsa

Retrieves voice agents from your Hamsa project.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/voice-agents`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [List Voice Agents](https://docs.tryhamsa.com/api-reference/endpoint/list-voice-agents-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language[]` | query | `array<string>` | no | Send multiple values as a array. |
| `search` | query | `string` | no | — |
| `skip` | query | `number` | no | — |
| `sortField` | query | `string` | no | Accepted values: `createdAt`. |
| `sortOrder` | query | `string` | no | Accepted values: `asc`, `desc`. |
| `take` | query | `number` | no | — |
| `type[]` | query | `array<string>` | no | Send multiple values as a array. |
