# Create Voice Agent with Hamsa

Creates a new voice agent in Hamsa.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice-agents`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Create Voice Agent](https://docs.tryhamsa.com/api-reference/endpoint/create-voice-agent)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agenticRag` | body | `boolean` | no |
| `agentName` | body | `string` | yes |
| `alignment` | body | `object` | no |
| `backgroundNoise` | body | `boolean` | no |
| `cancelNoisePer` | body | `string` | no |
| `description` | body | `string` | no |
| `enableAutoGainControl` | body | `boolean` | no |
| `greetingMessage` | body | `string` | no |
| `greetingMessageType` | body | `string` | no |
| `interrupt` | body | `boolean` | no |
| `knowledgeBaseItemsIds[]` | body | `array<string>` | no |
| `lang` | body | `string` | no |
| `languageDialectSwitcher` | body | `boolean` | no |
| `llmConfig` | body | `object` | no |
| `maxCallDuration` | body | `number` | no |
| `minInterruptionDuration` | body | `number` | no |
| `noiseCancellation` | body | `string` | no |
| `outcome` | body | `string` | no |
| `outcomeResponseShape` | body | `object` | no |
| `params` | body | `object` | no |
| `pokeMessages[]` | body | `array<string>` | no |
| `preamble` | body | `string` | no |
| `realTime` | body | `boolean` | no |
| `responseDelay` | body | `number` | no |
| `sendDenoisedToStt` | body | `boolean` | no |
| `silenceThreshold` | body | `number` | no |
| `speakerIdentification` | body | `boolean` | no |
| `thinkingVoice` | body | `boolean` | no |
| `tools` | body | `object` | no |
| `type` | body | `string` | no |
| `userInactivityTimeout` | body | `number` | no |
| `vadActivationThreshold` | body | `number` | no |
| `voiceDictionaryIds[]` | body | `array<string>` | no |
| `voiceId` | body | `string` | no |
| `waitForUserToSpeakFirst` | body | `number` | no |
| `webhookAuth` | body | `object` | no |
| `webhookUrl` | body | `string` | no |
| `webToolsIds[]` | body | `array<string>` | no |
| `webToolsOverrides` | body | `object` | no |
