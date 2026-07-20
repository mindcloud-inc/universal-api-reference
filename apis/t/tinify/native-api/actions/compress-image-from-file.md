# Compress Image From File with Tinify

Compresses an uploaded image file in Tinify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shrink`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Compress Image From File](https://tinify.com/developers/reference/http#compressing-images)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | AVIF, WebP, JPEG, or PNG image file to optimize. |
