# Replace Webhooks with Sendblue

Replaces webhooks in Sendblue.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/account/webhooks`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Replace Webhooks](https://docs.sendblue.com/api/resources/webhooks/methods/update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhooks.receive[]` | body | `array<string>` | no | Webhook URLs for inbound receive events. Send multiple values as a array. |
| `webhooks.outbound[]` | body | `array<string>` | no | Webhook URLs for outbound status events. Send multiple values as a array. |
| `webhooks.typing_indicator[]` | body | `array<string>` | no | Webhook URLs for typing indicator events. Send multiple values as a array. |
| `webhooks.call_log[]` | body | `array<string>` | no | Webhook URLs for call log events. Send multiple values as a array. |
| `webhooks.contact_created[]` | body | `array<string>` | no | Webhook URLs for contact-created events. Send multiple values as a array. |
| `webhooks.line_assigned[]` | body | `array<string>` | no | Webhook URLs for line-assigned events. Send multiple values as a array. |
| `webhooks.line_blocked[]` | body | `array<string>` | no | Webhook URLs for line-blocked events. Send multiple values as a array. |
| `webhooks.globalSecret` | body | `string` | no | Global secret applied to all webhook deliveries. |
