# Make Voice Call with CRM Messaging

Starts a voice call in CRM Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `https://campaigns.crm-messaging.cloud/api/voice-call`
- **Base URL:** `https://app.crm-messaging.cloud`
- **Official documentation:** [Make Voice Call](https://crm-messaging.cloud/docs/make-voice-calls-by-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `toNumber` | body | `string` | yes |
| `fromNumber` | body | `string` | yes |
| `content` | body | `string` | no |
| `messageType` | body | `string` | no |
| `voice` | body | `string` | no |
| `audioUrl` | body | `string` | no |
