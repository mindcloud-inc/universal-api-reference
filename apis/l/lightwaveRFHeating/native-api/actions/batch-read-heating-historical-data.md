# Batch Read Heating Historical Data with LightwaveRF Heating

Retrieves historical heating data from LightwaveRF Heating in batch.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/data`
- **Base URL:** `https://publicapi.lightwaverf.com`
- **Official documentation:** [Batch Read Heating Historical Data](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `devices[]` | body | `array<object>` | yes | The list of heating devices whose historical data should be read. |
| `start` | query | `number` | no | The earliest timestamp to include in the batch historical data query. |
| `end` | query | `number` | no | The latest timestamp to include in the batch historical data query. |
