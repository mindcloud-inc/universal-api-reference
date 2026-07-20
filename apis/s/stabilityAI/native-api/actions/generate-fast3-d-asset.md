# Generate Fast 3D Asset with Stability AI

Creates a 3D asset in Stability AI from one image.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2beta/3d/stable-fast-3d`
- **Base URL:** `https://api.stability.ai`
- **Official documentation:** [Generate Fast 3D Asset](https://platform.stability.ai/docs/api-reference#tag/3D/paths/~1v2beta~13d~1stable-fast-3d/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `model/gltf-binary` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image` | body | `file` | yes | Source image file used to generate the 3D asset. |
