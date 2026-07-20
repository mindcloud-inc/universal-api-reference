# Kling Multi Image To Image with CometAPI

Creates a Kling image from multiple images in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/images/generations`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Multi Image To Image](https://apidoc.cometapi.com/api/video/kling/multi-image-to-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject_image_list[]` | body | `array<object>` | yes | Subject image list. |
