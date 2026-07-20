# Generate text to video with 1minAI

Creates a video from text in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate text to video](https://docs.1min.ai/docs/api/ai-for-video/text-to-video/sora-text-to-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | — |
| `seconds` | body | `list` | no | Accepted values: `12 seconds`, `4 seconds`, `8 seconds`. |
| `size` | body | `list` | no | Accepted values: `1280x720`, `720x1280`. |
