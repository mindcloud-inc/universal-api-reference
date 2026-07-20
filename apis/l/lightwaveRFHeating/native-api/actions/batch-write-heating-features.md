# Batch Write Heating Features with LightwaveRF Heating

Updates multiple heating features in LightwaveRF Heating.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/features/write`
- **Base URL:** `https://publicapi.lightwaverf.com`
- **Official documentation:** [Batch Write Heating Features](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `features[]` | body | `array<object>` | yes | The list of heating feature writes to apply in one request. |
