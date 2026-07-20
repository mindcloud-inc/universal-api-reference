# Sketch Control with Dreamstudio

Creates an image from a sketch in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/sketch`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Sketch Control](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt describing the generated image. |
| `image` | body | `file` | yes | Guide image used for the sketch control request. |
