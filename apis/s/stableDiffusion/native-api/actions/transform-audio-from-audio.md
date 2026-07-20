# Transform Audio From Audio with Stable Diffusion

Transforms audio from an input clip in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/audio-to-audio`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Transform Audio From Audio](https://platform.stability.ai/docs/api-reference#tag/Stable%20Audio%202/paths/~1v2beta~1audio~1stable-audio-2~1audio-to-audio/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio` | body | `string` | yes | Source audio clip to transform. |
| `prompt` | body | `string` | yes | Text prompt describing the transformed audio output. |
