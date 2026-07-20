# Crop Image with 1001fx

Crops an image by width, height, and coordinates.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/cropimage`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Crop Image](https://1001fx.com/functions/cropimage)

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
| `x` | body | `number` | no |
| `y` | body | `number` | no |
