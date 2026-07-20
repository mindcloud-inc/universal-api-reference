# Compress Image From URL with TinyPNG

Compresses an image from a URL with TinyPNG.

## Endpoint

- **Method:** `POST`
- **Path:** `/shrink`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Compress Image From URL](https://tinify.com/developers/reference/http#compressing-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source.url` | body | `string` | yes | Public URL of the image to optimize with TinyPNG. |
