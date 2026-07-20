# Runway Video Upscale with CometAPI

Creates a Runway video upscale task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/runwayml/v1/video_upscale`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Runway Video Upscale](https://apidoc.cometapi.com/api/video/runway/official-format/upscale-a-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Upscale model. |
| `videoUri` | body | `string` | yes | Video URI. |
