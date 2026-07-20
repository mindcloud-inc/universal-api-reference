# Get Recording with DialMyCalls

Retrieves a recording from DialMyCalls.

## Endpoint

- **Method:** `GET`
- **Path:** `/recording/:RecordingId`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Get Recording](https://www.dialmycalls.com/api-documentation#recording-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RecordingId` | path | `string` | yes | The DialMyCalls recording ID to retrieve. |
