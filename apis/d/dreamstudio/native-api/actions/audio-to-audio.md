# Audio to Audio with Dreamstudio

Creates audio from an audio sample in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/audio-to-audio`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Audio to Audio](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt used to transform the input audio. |
| `audio` | body | `file` | yes | Input audio file to transform. |
