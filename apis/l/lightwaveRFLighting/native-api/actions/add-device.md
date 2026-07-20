# Add Device with LightwaveRF Lighting

Adds a device to LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/device/add`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Add Device](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The new device name. |
| `type` | body | `string` | yes | The LightwaveRF device type. |
| `destinationId` | body | `string` | yes | The destination identifier the device should be added to. |
| `productCode` | body | `string` | yes | The LightwaveRF product code for the device. |
| `manufacturerCode` | body | `string` | yes | The manufacturer code for the device. |
| `parentGroups` | body | `string` | yes | The parent group identifiers that should contain the device. |
