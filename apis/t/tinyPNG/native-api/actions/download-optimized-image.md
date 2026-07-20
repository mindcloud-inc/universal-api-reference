# Download Optimized Image with TinyPNG

Downloads an optimized image from TinyPNG.

## Endpoint

- **Method:** `GET`
- **Path:** `{{outputPath}}`
- **Base URL:** `https://api.tinify.com`
- **Official documentation:** [Download Optimized Image](https://tinify.com/developers/reference/http#compressing-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputPath` | path | `string` | yes | TinyPNG output path returned by a previous action, for example `/output/abc123`. |
