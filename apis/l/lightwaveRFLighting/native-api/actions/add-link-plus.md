# Add LinkPlus with LightwaveRF Lighting

Adds a Link Plus to LightwaveRF Lighting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/linkplus/add`
- **Base URL:** `https://publicapi.lightwaverf.com/`
- **Official documentation:** [Add LinkPlus](https://jsapi.apiary.io/apis/linkpluspublicapi.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destinationId` | body | `string` | yes | The destination identifier used when adding a LinkPlus hub. |
| `authType` | body | `string` | yes | The authentication type for the LinkPlus pairing request. |
| `rootGroupId` | body | `string` | yes | The root structure group identifier that should own the LinkPlus hub. |
