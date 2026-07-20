# Convert Image To AVIF with TinyPNG

Creates an AVIF image from TinyPNG output.

## Endpoint

- **Method:** `POST`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Convert Image To AVIF](https://tinify.com/developers/reference/http#converting-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
