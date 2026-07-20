# Set Heating Feature with LightwaveRF Heating

Updates an existing heating feature in LightwaveRF Heating.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/feature/{featureId}`
- **Base URL:** `https://publicapi.lightwaverf.com`
- **Official documentation:** [Set Heating Feature](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `featureId` | path | `string` | yes | The LightwaveRF heating feature identifier to update. |
| `value` | body | `number` | yes | The numeric value to write to the heating feature. |
