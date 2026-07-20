# Update Webhook with LightwaveRF Lighting

Updates an existing webhook in LightwaveRF Lighting.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/events/{eventId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Update Webhook](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The LightwaveRF webhook identifier to update. |
| `events[]` | body | `array<object>` | yes | The updated list of LightwaveRF event subscriptions for the webhook. |
| `url` | body | `string` | yes | The public HTTPS URL that should receive webhook deliveries. |
| `ref` | body | `string` | no | An optional reference string to correlate the webhook registration. |
| `version` | body | `number` | yes | The current webhook version required by the provider for optimistic concurrency. |
