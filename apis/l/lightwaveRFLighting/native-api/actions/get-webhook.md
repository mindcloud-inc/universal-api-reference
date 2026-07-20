# Get Webhook with LightwaveRF Lighting

Retrieves a webhook from LightwaveRF Lighting.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events/{eventId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Get Webhook](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The LightwaveRF webhook identifier to retrieve. |
