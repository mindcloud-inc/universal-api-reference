# Image To Video with Runway

Creates a video generation task from an image in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/image_to_video`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Image To Video](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1image_to_video/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Generation model, such as gen4.5, gen4_turbo, gen3a_turbo, veo3.1, veo3.1_fast, or veo3. |
| `promptImage` | body | `string` | yes | HTTPS URL, Runway URI, or data URI for the source image. |
| `promptText` | body | `string` | yes | Detailed text prompt for the video generation. |
| `ratio` | body | `string` | yes | Aspect ratio for the output video. Example: 1280:720. |
| `duration` | body | `number` | yes | Output duration in seconds. |
