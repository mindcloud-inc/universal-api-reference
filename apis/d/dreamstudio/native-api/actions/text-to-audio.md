# Text to Audio with Dreamstudio

Creates audio from a text prompt in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/text-to-audio`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Text to Audio](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt used to generate audio. |
| `output_format` | body | `string` | no | Optional output file format for the generated audio. |
