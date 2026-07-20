# Generate Audio From Text with Stability AI

Creates audio in Stability AI from a text prompt.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/text-to-audio`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate Audio From Text](https://platform.stability.ai/docs/api-reference#tag/Stable-Audio-2/paths/~1v2beta~1audio~1stable-audio-2~1text-to-audio/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the audio to generate. |
