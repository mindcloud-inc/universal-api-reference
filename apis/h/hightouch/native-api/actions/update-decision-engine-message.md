# Update Decision Engine Message with Hightouch

Updates a decision engine message in Hightouch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/decision-engine/flow/{flowId}/messages/{messageId}`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Update Decision Engine Message](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `string` | yes | The Decision Engine flow ID. |
| `name` | body | `string` | no | The message name. |
| `messageId` | path | `string` | yes | The Decision Engine message ID. |
| `config` | body | `object` | no | Message configuration object. |
| `tags` | body | `object` | no | Message tags. |
| `guardrails` | body | `object` | no | Message guardrail settings. |
| `variables[]` | body | `array<object>` | no | Message variables. |
