# Resize Image with Mallabe

Creates a resized image in Mallabe.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/resize`
- **Base URL:** `https://mallabe.p.rapidapi.com/v1`
- **Official documentation:** [Resize Image](https://app.mallabe.com/images/resize/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Publicly accessible image URL. |
| `base64Image` | body | `string` | no | Base64-encoded image data. |
| `strategy` | body | `number` | yes | Resize strategy code from the Mallabe docs. |
| `width` | body | `number` | no | Target width or scale width value. |
| `height` | body | `number` | no | Target height or scale height value. |
| `removeExif` | body | `boolean` | no | Remove EXIF metadata from the output image. |
| `webhookUrl` | body | `string` | no | Webhook URL for asynchronous callbacks. |
| `fileName` | body | `string` | no | Output file name without extension. |
| `fileExtension` | body | `string` | no | Output image file extension. |
