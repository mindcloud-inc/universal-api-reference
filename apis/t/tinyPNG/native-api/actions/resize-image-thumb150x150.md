# Resize Image Thumb 150x150 with TinyPNG

Creates a TinyPNG thumbnail resized to 150x150.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Resize Image Thumb 150x150](https://tinify.com/developers/reference/http#resizing-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example /output/abc123. |
