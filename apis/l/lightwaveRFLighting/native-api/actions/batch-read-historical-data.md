# Batch Read Historical Data with LightwaveRF Lighting

Retrieves historical data for multiple features from LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/data`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Batch Read Historical Data](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devices[]` | body | `array<object>` | yes | The list of devices whose historical data should be read. |
| `start` | query | `number` | no | The earliest timestamp to include in the batch historical data query. |
| `end` | query | `number` | no | The latest timestamp to include in the batch historical data query. |
