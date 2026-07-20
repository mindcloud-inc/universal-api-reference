# Resize Image with 1001fx

Resizes an image to specified dimensions.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/resizeimage`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Resize Image](https://1001fx.com/functions/resizeimage)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `height` | body | `number` | no |
| `width` | body | `number` | no |
