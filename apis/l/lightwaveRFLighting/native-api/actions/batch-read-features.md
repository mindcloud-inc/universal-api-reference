# Batch Read Features with LightwaveRF Lighting

Retrieves multiple features from LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/features/read`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Batch Read Features](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `features[]` | body | `array<object>` | yes | The list of feature identifiers to read in one request. |
