# Kling Identify Face with CometAPI

Identifies faces for Kling lip-sync in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/videos/identify-face`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Identify Face](https://apidoc.cometapi.com/api/video/kling/lip-sync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_url` | body | `string` | yes | Video URL for face identification. |
