# Assign Twilio Number to Voice Agent with Hamsa

Assigns a Twilio number to a Hamsa voice agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice-agents/twilio/assign-number`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Assign Twilio Number to Voice Agent](https://docs.tryhamsa.com/api-reference/endpoint/assign-twilio-number)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `twilioPhoneNumber` | body | `string` | yes |
| `voiceAgentId` | body | `string` | yes |
