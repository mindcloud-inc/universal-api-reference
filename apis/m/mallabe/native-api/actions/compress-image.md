# Compress Image with Mallabe

Creates a compressed image in Mallabe.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/compress`
- **Base URL:** `https://mallabe.p.rapidapi.com/v1`
- **Official documentation:** [Compress Image](https://rapidapi.com/mallabe1/api/mallabe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | Publicly accessible image URL. |
| `base64Image` | body | `string` | no | Base64-encoded image data. |
| `quality` | body | `number` | yes | Compression quality for the output image. |
| `fileName` | body | `string` | no | Output file name without extension. |
| `fileExtension` | body | `string` | no | Output image file extension. |
