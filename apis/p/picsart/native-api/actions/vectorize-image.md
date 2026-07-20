# Vectorize Image with Picsart

Creates an SVG image from a raster image in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/vectorizer`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Vectorize Image](https://docs.picsart.io/reference/image-vectorize-raster-to-svg)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL. |
| `downscale_to` | body | `number` | no | Optional maximum size used before vectorization. |
