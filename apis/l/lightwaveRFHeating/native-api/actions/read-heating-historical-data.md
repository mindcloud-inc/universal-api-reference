# Read Heating Historical Data with LightwaveRF Heating

Retrieves historical heating data from LightwaveRF Heating.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/data/{deviceId}/{featureId}`
- **Base URL:** `https://publicapi.lightwaverf.com`
- **Official documentation:** [Read Heating Historical Data](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | The LightwaveRF heating device identifier whose historical data should be read. |
| `featureId` | path | `string` | yes | The LightwaveRF heating feature identifier whose historical data should be read. |
| `start` | query | `number` | no | The earliest timestamp in milliseconds to include in the historical data query. |
| `end` | query | `number` | no | The latest timestamp in milliseconds to include in the historical data query. |
| `limit` | query | `number` | no | The maximum number of historical records to return. |
