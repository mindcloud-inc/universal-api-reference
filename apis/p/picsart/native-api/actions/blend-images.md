# Blend Images with Picsart

Creates a blended image in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/blend`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Blend Images](https://docs.picsart.io/reference/image-blend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Base image URL. |
| `overlay_image_url` | body | `string` | yes | Overlay image URL. |
| `opacity` | body | `number` | no | Overlay opacity from 0 to 100. |
| `blend_mode` | body | `string` | no | Choose how the overlay blends with the base image. |
| `format` | body | `string` | no | Optional output image format. |
