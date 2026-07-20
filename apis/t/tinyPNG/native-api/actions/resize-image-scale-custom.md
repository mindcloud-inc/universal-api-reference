# Resize Image Scale Custom with TinyPNG

Creates a TinyPNG image scaled to a custom size.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Resize Image Scale Custom](https://tinify.com/developers/reference/http#resizing-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
| `resize.width` | body | `number` | no | Target width in pixels. Use either width or height, but not both. |
| `resize.height` | body | `number` | no | Target height in pixels. Use either width or height, but not both. |
