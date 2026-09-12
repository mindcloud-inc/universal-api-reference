# Verify Webhook Endpoint with Ramp

## Endpoint

- **Method:** `POST`
- **Path:** `webhooks/:webhookId/verify`
- **Base URL:** `https://api.ramp.com/developer/v1/`
- **Official documentation:** [Verify Webhook Endpoint](https://docs.ramp.com/developer-api/v1/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `challenge` | body | `string` | yes | The challenge that was sent to the webhook by Ramp. This will happen right after the webhook is first registered. |
| `webhookId` | path | `string` | yes | The ID received from Ramp when the webhook was registered. |
