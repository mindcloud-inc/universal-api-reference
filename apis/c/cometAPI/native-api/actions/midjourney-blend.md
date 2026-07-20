# Midjourney Blend with CometAPI

Creates a Midjourney blend task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/mj/submit/blend`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Midjourney Blend](https://apidoc.cometapi.com/api/image/midjourney/blend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `base64Array[]` | body | `array<string>` | yes | Base64 image array. |
