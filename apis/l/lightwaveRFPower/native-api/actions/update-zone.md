# Update Zone with LightwaveRF Power

Updates an existing zone in LightwaveRF Power.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/zone/{zoneId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Update Zone](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `zoneId` | path | `string` | yes | The LightwaveRF zone identifier to update. |
| `name` | body | `string` | no | The updated zone name. |
| `order[]` | body | `array<string>` | no | The ordered list of room identifiers within the zone. |
