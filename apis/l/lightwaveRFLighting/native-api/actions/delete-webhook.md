# Delete Webhook with LightwaveRF Lighting

Deletes an existing webhook from LightwaveRF Lighting.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/events/{eventId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Delete Webhook](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | The LightwaveRF webhook identifier to delete. |
