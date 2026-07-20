# Add Webhooks with Sendblue

Adds webhooks to Sendblue.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/account/webhooks`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Add Webhooks](https://docs.sendblue.com/api/resources/webhooks/methods/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhooks[]` | body | `array<string>` | yes | Webhook URLs to append. Send multiple values as a array. |
| `globalSecret` | body | `string` | no | Global secret for webhook signature verification. |
| `type` | body | `string` | no | The webhook event type to add. |
