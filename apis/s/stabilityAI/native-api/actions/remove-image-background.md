# Remove Image Background with Stability AI

Removes an image background in Stability AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/remove-background`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Remove Image Background](https://platform.stability.ai/docs/api-reference#tag/Edit/paths/~1v2beta~1stable-image~1edit~1remove-background/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file whose background should be removed. |
