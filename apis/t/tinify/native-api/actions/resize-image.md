# Resize Image with Tinify

Resizes an optimized image in Tinify.

## Endpoint

- **Method:** `POST`
- **Path:** `/output/:outputId`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Resize Image](https://tinify.com/developers/reference/http#resizing-images)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputId` | path | `string` | yes | Tinify output identifier from a prior compression URL. |
| `resize.method` | body | `list` | yes | Resize method. Scale needs width or height; fit, cover, and thumb need width and height. Accepted values: `0`, `1`, `2`, `3`. |
| `resize.width` | body | `number` | no | Target width in pixels. |
| `resize.height` | body | `number` | no | Target height in pixels. |
