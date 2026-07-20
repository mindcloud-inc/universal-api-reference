# Image - Rotate with Encodian - Image

Creates a rotated image in Encodian - Image.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Image/RotateImage`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Image - Rotate](https://support.encodian.com/hc/en-gb/articles/10041551840796)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64 content of the source image file. |
| `rotationAngle` | body | `number` | no | Number of degrees to rotate the image. |
| `presetRotationAngle` | body | `list` | no | Preset rotation angle to apply. Accepted values: `None`, `Rotate180`, `Rotate270`, `Rotate90`. |
| `resizeProportionally` | body | `boolean` | no | Adjust image dimensions proportionately to fit the rotated rectangle. |
| `backgroundColour` | body | `string` | no | Background colour used when Proportionate Resize is enabled. |
