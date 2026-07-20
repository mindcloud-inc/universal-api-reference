# Set Feature with LightwaveRF Lighting

Updates a feature value in LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/feature/{featureId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Set Feature](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureId` | path | `string` | yes | The LightwaveRF feature identifier to update. |
| `value` | body | `number` | yes | The numeric value to write to the feature. |
