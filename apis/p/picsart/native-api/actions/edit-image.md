# Edit Image with Picsart

Creates an edited image in Picsart.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/1.0/edit`
- **Base URL:** `https://api.picsart.io`
- **Official documentation:** [Edit Image](https://docs.picsart.io/reference/image-edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | yes | Source image URL. |
| `mode` | body | `string` | no | Choose crop or resize mode when applying dimensions. |
| `width` | body | `number` | no | Output width in pixels. |
| `height` | body | `number` | no | Output height in pixels. |
| `flip` | body | `string` | no | Flip the image horizontally or vertically. |
| `rotate` | body | `number` | no | Rotate the image between -180 and 180 degrees. |
| `format` | body | `string` | no | Optional output image format. |
