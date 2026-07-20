# Kling Create Video Edit Task with CometAPI

Creates a Kling multimodal edit task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/kling/v1/videos/multi-elements`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Kling Create Video Edit Task](https://apidoc.cometapi.com/api/video/kling/multimodal-video-editing/create-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit_mode` | body | `string` | yes | Video edit mode. |
| `prompt` | body | `string` | yes | Edit prompt. |
| `session_id` | body | `string` | yes | Session identifier. |
