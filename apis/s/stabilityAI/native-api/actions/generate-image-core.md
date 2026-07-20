# Generate Image Core with Stability AI

Creates an image in Stability AI with Core.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/generate/core`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate Image Core](https://platform.stability.ai/docs/api-reference#tag/Generate/paths/~1v2beta~1stable-image~1generate~1core/post)

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
