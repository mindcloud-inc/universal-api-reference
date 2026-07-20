# Edit Video with Grok

Updates a video in Grok with prompt-based edits.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/videos/edits`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Edit Video](https://docs.x.ai/developers/rest-api-reference/inference/videos#video-edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | xAI video editing model. |
| `prompt` | body | `string` | yes | Instructions describing the video edit. |
| `video` | body | `object` | yes | Source video file or URL to edit. |
