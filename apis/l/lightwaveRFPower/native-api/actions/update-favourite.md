# Update Favourite with LightwaveRF Power

Updates an existing favourite in LightwaveRF Power.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/favourite/{favouriteId}`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Update Favourite](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `favouriteId` | path | `string` | yes | The LightwaveRF favourite identifier to update. |
| `order[]` | body | `array<string>` | no | The ordered list of feature set identifiers for the favourite. |
