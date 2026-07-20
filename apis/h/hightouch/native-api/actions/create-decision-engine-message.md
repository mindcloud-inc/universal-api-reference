# Create Decision Engine Message with Hightouch

Creates a decision engine message in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/decision-engine/flow/{flowId}/messages`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Create Decision Engine Message](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `string` | yes | The Decision Engine flow ID. |
| `name` | body | `string` | yes | The message name. |
| `channelId` | body | `string` | yes | The channel ID for the message. |
| `config` | body | `object` | yes | Message configuration object. |
| `tags` | body | `object` | no | Message tags. |
| `guardrails` | body | `object` | no | Message guardrail settings. |
| `variables[]` | body | `array<object>` | no | Message variables. |
