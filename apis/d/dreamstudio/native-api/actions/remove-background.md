# Remove Background with Dreamstudio

Removes the background from an image in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/stable-image/edit/remove-background`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Remove Background](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Image file to remove the background from. |
