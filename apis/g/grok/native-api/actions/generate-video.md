# Generate Video with Grok

Creates a video generation request in Grok.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/videos/generations`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Generate Video](https://docs.x.ai/developers/rest-api-reference/inference/videos#video-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | xAI video generation model. |
| `prompt` | body | `string` | yes | Text prompt describing the video to generate. |
| `image` | body | `object` | no | Optional source image for image-to-video generation. |
| `duration` | body | `number` | no | Desired video duration in seconds. |
| `aspect_ratio` | body | `string` | no | Desired output aspect ratio. |
| `resolution` | body | `string` | no | Desired output resolution. |
