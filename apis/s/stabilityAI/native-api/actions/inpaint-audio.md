# Inpaint Audio with Stability AI

Updates audio in Stability AI with inpainting.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/inpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Inpaint Audio](https://platform.stability.ai/docs/api-reference#tag/Stable-Audio-2/paths/~1v2beta~1audio~1stable-audio-2~1inpaint/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the desired audio inpaint. |
| `audio` | body | `file` | yes | Source audio file to inpaint. |
