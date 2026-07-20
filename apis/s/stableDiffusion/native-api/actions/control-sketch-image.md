# Control Sketch Image with Stable Diffusion

Generates an image from a sketch in Stable Diffusion.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/sketch`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Control Sketch Image](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1sketch/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `string` | yes | Sketch or control image. |
| `prompt` | body | `string` | yes | Text prompt describing the output image. |
