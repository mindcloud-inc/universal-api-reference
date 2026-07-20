# Kling Add Video Selection with CometAPI

Adds a Kling video selection in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/videos/multi-elements/add-selection`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Add Video Selection](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/add-video-selection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frame_index` | body | `number` | yes | Frame index. |
| `points[]` | body | `array<object>` | yes | Selection points. |
| `session_id` | body | `string` | yes | Session identifier. |
