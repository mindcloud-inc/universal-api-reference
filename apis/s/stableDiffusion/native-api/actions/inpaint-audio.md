# Inpaint Audio with Stable Diffusion

Inpaints audio in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/inpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Inpaint Audio](https://platform.stability.ai/docs/api-reference#tag/Stable%20Audio%202/paths/~1v2beta~1audio~1stable-audio-2~1inpaint/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio` | body | `string` | yes | Source audio clip to inpaint. |
| `prompt` | body | `string` | yes | Text prompt describing the desired repaired audio output. |
