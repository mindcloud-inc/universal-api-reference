# Assign Phone Number to Voice Agent with Hamsa

Assigns a phone number to a Hamsa voice agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice-agents/assign-number`
- **Base URL:** `https://api.tryhamsa.com`
- **Official documentation:** [Assign Phone Number to Voice Agent](https://docs.tryhamsa.com/api-reference/endpoint/assign-phone-number)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `phoneNumber` | body | `string` | yes |
| `voiceAgentId` | body | `string` | yes |
