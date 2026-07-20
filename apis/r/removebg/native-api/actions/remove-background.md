# Remove Background with Remove.bg

Creates a background-removed image in Remove.bg.

## Endpoint

- **Method:** `POST`
- **Path:** `/removebg`
- **Base URL:** `https://api.remove.bg/v1.0`
- **Official documentation:** [Remove Background](https://www.remove.bg/api#api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_url` | body | `string` | no | Source image URL. Provide exactly one image source. |
| `image_file_b64` | body | `string` | no | Base64-encoded source image. Provide exactly one image source. |
| `size` | body | `list` | no | Maximum output image resolution. Accepted values: `auto`, `full`, `preview`. |
| `type` | body | `list` | no | Detect or set the foreground type. Accepted values: `animal`, `auto`, `car`, `graphic`, `person`, `product`, `transportation`. |
| `type_level` | body | `list` | no | Classification level for the detected foreground type. Accepted values: `1`, `2`, `latest`, `none`. |
| `format` | body | `list` | no | Result image format. Accepted values: `auto`, `jpg`, `png`, `webp`, `zip`. |
| `roi` | body | `string` | no | Rectangle region where foreground detection is allowed. |
| `crop` | body | `boolean` | no | Crop empty regions from the result. |
| `crop_margin` | body | `string` | no | Margin to add around the cropped subject. |
| `scale` | body | `string` | no | Scale the subject relative to the image size. |
| `position` | body | `string` | no | Position the subject within the image canvas. |
| `channels` | body | `list` | no | Return the final image or only the alpha mask. Accepted values: `alpha`, `rgba`. |
| `shadow_type` | body | `string` | no | Generate shadows based on the detected or selected foreground type. |
| `shadow_opacity` | body | `string` | no | Shadow darkness from 0 to 100 or auto. |
| `semitransparency` | body | `boolean` | no | Keep semi-transparent regions in the result where supported. |
| `bg_color` | body | `string` | no | Solid background color to add behind the subject. |
| `bg_image_url` | body | `string` | no | Background image URL to place behind the subject. |
