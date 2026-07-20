# Generate 3D Model with Dreamstudio

Creates a 3D model from an image in Dreamstudio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/3d/stable-fast-3d`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate 3D Model](https://platform.stability.ai/docs/api-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Single image file used to generate a 3D model. |
