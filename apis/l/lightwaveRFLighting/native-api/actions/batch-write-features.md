# Batch Write Features with LightwaveRF Lighting

Updates multiple features in LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/features/write`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Batch Write Features](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `features[]` | body | `array<object>` | yes | The list of feature writes to apply in one request. |
