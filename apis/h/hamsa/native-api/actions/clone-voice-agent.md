# Clone Voice Agent with Hamsa

Clones a voice agent in Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice-agents/clone`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Clone Voice Agent](https://docs.tryhamsa.com/api-reference/endpoint/clone-voice-agent)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentName` | body | `string` | yes |
| `voiceAgentId` | query | `string` | yes |
