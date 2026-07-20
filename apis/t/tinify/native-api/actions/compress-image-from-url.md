# Compress Image From URL with Tinify

Compresses an image from a URL in Tinify.

## Endpoint

- **Method:** `POST`
- **Path:** `/shrink`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Compress Image From URL](https://tinify.com/developers/reference/http#compressing-images)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source.url` | body | `string` | yes | Publicly reachable AVIF, WebP, JPEG, or PNG image URL to optimize. |
