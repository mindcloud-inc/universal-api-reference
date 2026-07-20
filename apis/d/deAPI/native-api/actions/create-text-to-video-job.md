# Create Text-to-Video Job with deAPI

Creates a text-to-video job in deAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/client/txt2video`
- **Base URL:** `https://api.deapi.ai`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fps` | body | `string` | no | Frames per second for the generated video. |
| `frames` | body | `string` | no | Number of frames to generate. |
| `guidance` | body | `string` | no | Guidance scale for generation. |
| `height` | body | `string` | no | Video height in pixels. |
| `model` | body | `string` | no | Video model slug from List Models. |
| `negative_prompt` | body | `string` | no | Elements to avoid in the generated video. |
| `prompt` | body | `string` | no | Main prompt for video generation. |
| `seed` | body | `string` | no | Random seed for generation. |
| `steps` | body | `string` | no | Number of inference steps. |
| `width` | body | `string` | no | Video width in pixels. |
