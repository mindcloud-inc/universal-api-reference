# Control Sketch Image with Stability AI

Creates an image in Stability AI from a sketch.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/sketch`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Control Sketch Image](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1sketch/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the desired output. |
| `image` | body | `file` | yes | Sketch or control image file. |
