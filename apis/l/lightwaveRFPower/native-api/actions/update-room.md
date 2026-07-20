# Update Room with LightwaveRF Power

Updates an existing room in LightwaveRF Power.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/room/{roomId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Update Room](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roomId` | path | `string` | yes | The LightwaveRF room identifier to update. |
| `name` | body | `string` | no | The updated room name. |
