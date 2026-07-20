# Generate Audio From Text with Stable Diffusion

Generates audio from text in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/text-to-audio`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate Audio From Text](https://platform.stability.ai/docs/api-reference#tag/Stable%20Audio%202/paths/~1v2beta~1audio~1stable-audio-2~1text-to-audio/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the audio to generate. |
