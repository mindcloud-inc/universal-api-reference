# Generate Image Ultra with Stability AI

Creates an image in Stability AI with Ultra.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/generate/ultra`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate Image Ultra](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1ultra/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the image to generate. |
