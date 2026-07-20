# Batch Read Heating Features with LightwaveRF Heating

Retrieves multiple heating features from LightwaveRF Heating.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/features/read`
- **Base URL:** `https://publicapi.lightwaverf.com`
- **Official documentation:** [Batch Read Heating Features](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `features[]` | body | `array<object>` | yes | The list of heating feature identifiers to read in one request. |
