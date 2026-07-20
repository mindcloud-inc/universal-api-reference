# Remove Background with Picsart

Creates a background-removed image in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/removebg`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Remove Background](https://docs.picsart.io/reference/image-remove-background)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL. |
| `output_type` | body | `string` | no | Select cutout or mask output. |
| `bg_color` | body | `string` | no | Optional solid background color. |
| `format` | body | `string` | no | Optional output image format. |
