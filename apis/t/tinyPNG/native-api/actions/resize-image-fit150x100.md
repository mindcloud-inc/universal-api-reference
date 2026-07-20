# Resize Image Fit 150x100 with TinyPNG

Creates a TinyPNG image resized to fit 150x100.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Resize Image Fit 150x100](https://tinify.com/developers/reference/http#resizing-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
