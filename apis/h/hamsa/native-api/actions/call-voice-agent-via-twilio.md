# Call Voice Agent via Twilio with Hamsa

Starts a Twilio call to a Hamsa voice agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice-agents/twilio/call`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Call Voice Agent via Twilio](https://docs.tryhamsa.com/api-reference/endpoint/call-twilio-number)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentDetails` | body | `object` | no |
| `params` | body | `object` | no |
| `toNumber` | body | `string` | yes |
| `twilioPhoneNumber` | body | `string` | yes |
| `voiceAgentId` | body | `string` | yes |
| `webhookAuth` | body | `object` | no |
| `webhookUrl` | body | `string` | no |
