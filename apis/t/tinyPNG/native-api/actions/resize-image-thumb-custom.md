# Resize Image Thumb Custom with TinyPNG

Creates a TinyPNG thumbnail with custom dimensions.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Resize Image Thumb Custom](https://tinify.com/developers/reference/http#resizing-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
| `resize.width` | body | `number` | yes | Target width in pixels. |
| `resize.height` | body | `number` | yes | Target height in pixels. |
