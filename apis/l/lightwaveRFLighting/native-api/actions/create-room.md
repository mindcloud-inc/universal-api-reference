# Create Room with LightwaveRF Lighting

Creates a new room in LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/room`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Create Room](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the new room. |
| `parentGroup` | body | `string` | yes | The parent zone group identifier that should contain the room. |
