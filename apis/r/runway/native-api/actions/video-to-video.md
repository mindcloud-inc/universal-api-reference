# Video To Video with Runway

Creates a video generation task from a video in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/video_to_video`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Video To Video](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1video_to_video/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Runway currently requires gen4_aleph for video to video. |
| `promptText` | body | `string` | yes | Detailed text prompt for the transformed output video. |
| `videoUri` | body | `string` | yes | HTTPS URL, Runway URI, or data URI for the source video. |
