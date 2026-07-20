# Text To Video with Runway

Creates a video generation task from text in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/text_to_video`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Text To Video](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1text_to_video/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `duration` | body | `number` | yes | Requested output duration in seconds, between 2 and 10. |
| `model` | body | `string` | yes | Generation model, such as gen4.5, veo3.1, veo3.1_fast, or veo3. |
| `promptText` | body | `string` | yes | Detailed text prompt for the video generation. |
| `ratio` | body | `string` | yes | Output video ratio, such as 1280:720 or 720:1280. |
