# Kling Multi Image To Video with CometAPI

Creates a Kling multi-image video in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/videos/multi-image2video`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Multi Image To Video](https://apidoc.cometapi.com/api/video/kling/multi-image-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `string` | yes | Video duration. |
| `image_list[]` | body | `array<object>` | yes | Image list. |
| `model_name` | body | `string` | yes | Kling model name. |
| `prompt` | body | `string` | yes | Video prompt. |
