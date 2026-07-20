# Inpaint Audio with Dreamstudio

Creates inpainted audio from a sample in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/audio/stable-audio-2/inpaint`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Inpaint Audio](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt used for the audio inpaint request. |
| `audio` | body | `file` | yes | Input audio file to inpaint. |
