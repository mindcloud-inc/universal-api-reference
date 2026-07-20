# Create Webhook with LightwaveRF Lighting

Creates a webhook in LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Create Webhook](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<object>` | yes | The list of LightwaveRF event subscriptions to register for the webhook. |
| `url` | body | `string` | yes | The public HTTPS URL that should receive webhook deliveries. |
| `ref` | body | `string` | no | An optional reference string to correlate the webhook registration. |
