# Update Voice Agent with Hamsa

Updates an existing voice agent in Hamsa.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/voice-agents/:voiceAgentId`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Update Voice Agent](https://docs.tryhamsa.com/api-reference/endpoint/update-voice-agent-v2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `callSettings` | body | `object` | no |
| `conversation` | body | `object` | no |
| `knowledgeBaseItemsIds[]` | body | `array<string>` | no |
| `llm` | body | `object` | no |
| `name` | body | `string` | no |
| `outcomeResponseShape` | body | `object` | no |
| `phoneNumber` | body | `object` | no |
| `tools[]` | body | `array<object>` | no |
| `type` | body | `string` | no |
| `voice` | body | `object` | no |
| `voiceAgentId` | path | `string` | yes |
| `voiceDictionaryIds[]` | body | `array<string>` | no |
| `webhookAuth` | body | `object` | no |
| `webhookUrl` | body | `string` | no |
| `workflow` | body | `object` | no |
