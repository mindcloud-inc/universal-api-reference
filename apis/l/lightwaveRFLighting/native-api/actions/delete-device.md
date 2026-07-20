# Delete Device with LightwaveRF Lighting

Deletes an existing device from LightwaveRF Lighting.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/device/delete/{deviceId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Delete Device](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | The LightwaveRF device identifier to delete. |
