# Control Structure Image with Stability AI

Creates an image in Stability AI from image structure.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/control/structure`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Control Structure Image](https://platform.stability.ai/docs/api-reference#tag/Control/paths/~1v2beta~1stable-image~1control~1structure/post)

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
| `image` | body | `file` | yes | Structure/control image file. |
