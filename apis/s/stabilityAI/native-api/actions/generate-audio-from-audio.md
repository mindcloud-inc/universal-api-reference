# Generate Audio From Audio with Stability AI

Creates audio in Stability AI from an audio sample.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/audio-to-audio`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate Audio From Audio](https://platform.stability.ai/docs/api-reference#tag/Stable-Audio-2/paths/~1v2beta~1audio~1stable-audio-2~1audio-to-audio/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the desired audio transformation. |
| `audio` | body | `file` | yes | Source audio file to transform. |
