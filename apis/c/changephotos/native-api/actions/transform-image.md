# Transform Image with change.photos

Creates a transformed image in change.photos.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/change`
- **Base URL:** `https://www.change.photos`
- **Official documentation:** [Transform Image](https://www.change.photos/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the image to transform. |
| `width` | body | `number` | no | Desired width of the output image. |
| `height` | body | `number` | no | Desired height of the output image. |
| `format` | body | `list<string>` | no | Output image format. Accepted values: `jpeg`, `png`, `webp`. |
| `quality` | body | `number` | no | Output image quality from 1 to 100. |
| `fit` | body | `list<string>` | no | How the image should fit within the dimensions. Accepted values: `contain`, `cover`, `fill`, `inside`, `outside`. |
| `flip` | body | `boolean` | no | Flip the image vertically. |
| `flop` | body | `boolean` | no | Flip the image horizontally. |
| `rotate` | body | `number` | no | Rotation angle in degrees from -360 to 360. |
| `grayscale` | body | `boolean` | no | Convert image to grayscale. |
| `blur` | body | `number` | no | Gaussian blur sigma value from 0.3 to 1000. |
| `sharpen` | body | `boolean` | no | Apply sharpening effect. |
| `compress` | body | `boolean` | no | Apply additional compression. |
| `tint.r` | body | `number` | no | Red component of the RGB tint, from 0 to 255. |
| `tint.g` | body | `number` | no | Green component of the RGB tint, from 0 to 255. |
| `tint.b` | body | `number` | no | Blue component of the RGB tint, from 0 to 255. |
